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


using System;

class StatementSample
{
   static void Main()
   {
      double x, y, z;  // 変数を宣言。

      // xにユーザーの入力した値を代入。
      Console.Write("input x : ");
      x = double.Parse(Console.ReadLine());

      // yにユーザーの入力した値を代入。
      Console.Write("input y : ");
      y = double.Parse(Console.ReadLine());

      // 入力された値を元に計算
      z = x * x + y * y; // z に x と y の二乗和を代入
      x /=  z;           // x =  x / z; と同じ。
      y /= -z;           // y = -y / z; と同じ。

      // 計算結果を出力
      Console.Write("({0}, {1})", x, y);
   }
}

// ほぼ同じ意味
Console.WriteLine(string.Format("{0,4:x}", x));
Console.WriteLine($"{x,4:x}");

// 書き方を忘れて、 , と : を間違えてしまうと…

// 実行時エラー
Console.WriteLine(string.Format("{0,x}", x));

// コンパイル エラー
Console.WriteLine($"{x,x}");

using System;

class CheckedSample
{
  static void Main()
  {
    try
    {
      checked
      {
        sbyte a = 64;
        sbyte b = 65;
        sbyte c = (sbyte)(a + b);
      }
    }
    catch(OverflowException ex)
    {
      Console.Write(ex.Message);
    }
  }
}
