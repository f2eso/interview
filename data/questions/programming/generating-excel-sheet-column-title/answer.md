## 循环方式

{% highlight js %}
function convert(num) {
  const result = [];

  let divided;

  do {
    const dividedNum = divided ? divided[0] : num;

    // 将数字处理成 `[商, 余数]` 的格式
    divided = isNaN(dividedNum) || dividedNum < 1 ? [-1, -1] : [~~(dividedNum / 26), dividedNum % 26];

    // 进位的特殊处理
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

{% highlight js %}
function convert(num) {
  return num <= 26 ? String.fromCharCode('A'.charCodeAt(0) - 1 + num) : convert(~~((num - 1) / 26)) + convert(num % 26 || 26);
}
{% endhighlight %}
