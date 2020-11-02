## 循环方式

用循环实现：

{% highlight js %}
function convert(num) {
  const result = [];

  let divided;

  do {
    const dividedNum = divided ? divided[0] : num;

    divided = isNaN(dividedNum) || dividedNum < 1 ? [-1, -1] : [~~(dividedNum / 26), dividedNum % 26];

    if (divided[1] === 0) {
      divided = [divided[0] - 1, 26];
    }

    if (divided[0] !== -1) {
      result.unshift(String.fromCharCode('A'.charCodeAt(0) - 1 + divided[1]));
    }
  } while (divided[0] / 26 > 0);

  return result.join('');
}
{% endhighlight %}

## 递归方式

用递归实现：

{% highlight js %}
function convert(num) {
  return num <= 26 ? String.fromCharCode('A'.charCodeAt(0) - 1 + num) : convert(~~((num - 1) / 26)) + convert(num % 26 || 26);
}
{% endhighlight %}
