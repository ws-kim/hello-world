# hello-world
tutorial repository
Hi! I'm WS KIM

/*
 この部分はコメントです。
 複数行にわたるコメントを書くことも可能です。
*/

// このようなコメントもかけます。
// 行末までがコメントになります。

/*
 でも、このコメントを
  /* こんな風に */
 2重に使っちゃだめ。
 このコメントはエラーになります。
*/


using System;

class Program
{
    static void Main()
    {
        // 入力を促すメッセージの表示して、文字を入力してもらう
        Console.Write("あなたのお名前は？ : ");
        var name = Console.ReadLine();

        // 入力を促すメッセージの表示して、数値を入力してもらう
        Console.Write("あなたのお年は？   : ");
        var age = int.Parse(Console.ReadLine());

        // メッセージの出力
        Console.WriteLine("{0} ({1}歳) さん、ようこそお越しくださいました。", name, age);
    }
}
