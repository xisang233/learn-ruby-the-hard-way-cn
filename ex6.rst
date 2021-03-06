习题 6: 字符串和文本
============================
虽然你已经在程序中写过字符串了，你还没学过它们的用处。
在这章习题中我们将使用复杂的字符串来建立一系列的变量，从中你将学到它们的用途。
首先我们解释一下字符串是什么东西。

字符串通常是指你想要展示给别人的、或者是你想要从程序里“导出”的一小段字符。
Ruby 可以通过文本里的双引号 ``"`` 或者单引号 ``'`` 识别出字符串来。
这在你以前的 ``puts`` 练习中你已经见过很多次了。
如果你把单引号或者双引号括起来的文本放到 ``puts`` 后面，它们就会被 Ruby 打印出来。

字符串可以包含格式化字符 ``%s``，这个你之前也见过的。
你只要将格式化的变量放到字符串中，再紧跟着一个百分号 ``%`` ，再紧跟着变量名即可。
唯一要注意的地方，是如果你想要在字符串中通过格式化字符放入多个变量的时候，
你需要将变量放到 ``[ ]`` 中，而且变量之间用 ``,`` 隔开。
就像你逛商店说”我要买牛奶、面包、鸡蛋、八宝粥”一样，只不过程序员说的是”[milk, eggs, bread, soup]”。

在字符串中插入变量的另一种方法是使用字符串插值  (string interpolation) 这种技巧。
方法是使用 ``#{}`` 。试着用这种方法格式化字符串吧：

.. code-block:: ruby

    name1 = "Joe" name2 = "Mary" puts "Hello %s, where is %s?" % [name1, name2] 

我们可以输入：

.. code-block:: ruby

    name1 = "Joe" name2 = "Mary" puts "Hello #{name1}, where is #{name2}?" 

我们将键入大量的字符串、变量、和格式化字符，并且将它们打印出来。
我们还将练习使用简写的变量名。
程序员喜欢使用恼人的难度的简写来节约打字时间，所以我们现在就提早学会这个，这样你就能读懂并且写出这些东西了。

.. literalinclude:: ex/ex6.rb
    :language: ruby
    :linenos:

你应该看到的
-------------------

::

    There are 10 types of people.
    Those who know binary and those who don't.
    I said: There are 10 types of people..
    I also said: 'Those who know binary and those who don't.'.
    Isn't that joke so funny?! false
    This is the left side of...a string with a right side.

加分习题
------------

1. 通读程序，在每一行的上面写一行注解，给自己解释一下这一行的作用。
2. 找到所有的”字符串包含字符串”的位置，总共有四个位置。
3. 你确定只有四个位置吗？你怎么知道的？没准我在骗你呢。
4. 解释一下为什么 ``w`` 和 ``e`` 用 ``+`` 连起来就可以生成一个更长的字符串。
