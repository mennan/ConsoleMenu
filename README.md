# Console Menu
[![Build status](https://ci.appveyor.com/api/projects/status/myb3cpel269xv0iu?svg=true)](https://ci.appveyor.com/project/arthurvaverko/consolemenu)
[![Nuget Version](https://img.shields.io/nuget/v/ConsoleUI.ConsoleMenu.svg)](https://www.nuget.org/packages/ConsoleUI.ConsoleMenu/)


A console base UI menu (old school) navigation using arrow keys

# How it looks

![](https://thumbs.gfycat.com/FlawedForkedHochstettersfrog-small.gif)


# Usage example
```C#
using ConsoleUI;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleMenuTest
{
	class Program
	{
		static void Main(string[] args)
		{
			var items = Enumerable.Range(1,20).Select(i => new ConsoleMenuItem($"Item{i}", itemCallback));
			var menu = new ConsoleMenu("This is a test menu", items);
			menu.RunConsoleMenu();
		}

		private static void itemCallback(string itemClicked)
		{
			Console.Clear();
			Console.WriteLine(itemClicked);
		}
	}
}
```


