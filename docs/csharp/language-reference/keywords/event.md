---
title: event - C# 参考
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- event
- remove
- event_CSharpKeyword
- add
helpviewer_keywords:
- event keyword [C#]
ms.assetid: 7858fd85-153b-4259-85d0-6aa13c35f174
ms.openlocfilehash: 9575d6e998ff709b06f1da21abd17a3629c17029
ms.sourcegitcommit: 26f4a7697c32978f6a328c89dc4ea87034065989
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2019
ms.locfileid: "66251041"
---
# <a name="event-c-reference"></a>event（C# 参考）
`event` 关键字用于声明发布服务器类中的事件。  
  
## <a name="example"></a>示例  
 下面的示例演示如何声明和引发使用 <xref:System.EventHandler> 作为基础委托类型的事件。 有关展示如何使用泛型 <xref:System.EventHandler%601> 委托类型以及如何订阅事件并创建事件处理程序方法的完整代码示例，请参阅[操作说明：发布符合 .NET Framework 准则的事件](../../../csharp/programming-guide/events/how-to-publish-events-that-conform-to-net-framework-guidelines.md)。  
  
 [!code-csharp[csrefKeywordsModifiers#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#7)]
  
 事件是一种特殊的多播委托，仅可以从声明事件的类或结构（发布服务器类）中对其进行调用。 如果其他类或结构订阅该事件，则在发布服务器类引发该事件时，将调用其事件处理程序方法。 有关详细信息和代码示例，请参阅[事件](../../../csharp/programming-guide/events/index.md)和[委托](../../../csharp/programming-guide/delegates/index.md)。  
  
 可以将事件标记为[public](../../../csharp/language-reference/keywords/public.md)、[private](../../../csharp/language-reference/keywords/private.md)、[protected](../../../csharp/language-reference/keywords/protected.md)、[internal](../../../csharp/language-reference/keywords/internal.md)、[protected internal](../../../csharp/language-reference/keywords/protected-internal.md) 或 [private protected](../../../csharp/language-reference/keywords/private-protected.md)。 这些访问修饰符定义该类的用户访问该事件的方式。 有关详细信息，请参阅[访问修饰符](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)。  
  
## <a name="keywords-and-events"></a>关键字和事件  
 下列关键字应用于事件。  
  
|关键字|说明|更多相关信息|  
|-------------|-----------------|--------------------------|  
|[static](../../../csharp/language-reference/keywords/static.md)|使事件可供调用方在任何时候进行调用，即使不存在类的实例。|[静态类和静态类成员](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md)|  
|[virtual](../../../csharp/language-reference/keywords/virtual.md)|允许派生类使用[重写](../../../csharp/language-reference/keywords/override.md)关键字重写事件行为。|[继承](../../../csharp/programming-guide/classes-and-structs/inheritance.md)|  
|[sealed](../../../csharp/language-reference/keywords/sealed.md)|指定对于派生类，它不再是虚拟的。||  
|[abstract](../../../csharp/language-reference/keywords/abstract.md)|编译器不会生成 `add` 和 `remove` 事件访问器块，因此派生类必须提供其自己的实现。||  
  
 可以通过使用[静态](../../../csharp/language-reference/keywords/static.md)关键字将事件声明为静态事件。 这可使事件可供调用方在任何时候进行调用，即使不存在类的实例。 有关详细信息，请参阅[静态类和静态类成员](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md)。  
  
 可以通过使用[虚拟](../../../csharp/language-reference/keywords/virtual.md)关键字将事件标记为虚事件。 这可使派生类使用[重写](../../../csharp/language-reference/keywords/override.md)关键字重写事件行为。 有关详细信息，请参阅[继承](../../../csharp/programming-guide/classes-and-structs/inheritance.md)。 重写虚拟事件的事件也可以为[密封](../../../csharp/language-reference/keywords/sealed.md)，指定对于派生类，它不再是虚拟的。 最后，可以声明事件为[抽象](../../../csharp/language-reference/keywords/abstract.md)，这意味着编译器将不会生成 `add` 和 `remove` 事件访问器块。 因此，派生类必须提供其自己的实现。  
  
## <a name="c-language-specification"></a>C# 语言规范  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>请参阅

- [C# 参考](../../../csharp/language-reference/index.md)
- [C# 编程指南](../../../csharp/programming-guide/index.md)
- [C# 关键字](../../../csharp/language-reference/keywords/index.md)
- [add](../../../csharp/language-reference/keywords/add.md)
- [remove](../../../csharp/language-reference/keywords/remove.md)
- [修饰符](../../../csharp/language-reference/keywords/modifiers.md)
- [如何：合并委托（多播委托）](../../../csharp/programming-guide/delegates/how-to-combine-delegates-multicast-delegates.md)
