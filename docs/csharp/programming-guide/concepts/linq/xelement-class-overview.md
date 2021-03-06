---
title: XElement 类概述 (C#)
ms.date: 07/20/2015
ms.assetid: 2b9f0cd8-a1d1-4037-accf-0f38a410fa11
ms.openlocfilehash: 815b7b6523afe7106fcdcbe242d667c5ad6aa56e
ms.sourcegitcommit: 155012a8a826ee8ab6aa49b1b3a3b532e7b7d9bd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2019
ms.locfileid: "66487019"
---
# <a name="xelement-class-overview-c"></a>XElement 类概述 (C#)
<xref:System.Xml.Linq.XElement> 类是 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] 中的基础类之一。 它表示一个 XML 元素。 可以使用该类创建元素；更改元素内容；添加、更改或删除子元素；向元素中添加属性；或以文本格式序列化元素内容。 还可以与 <xref:System.Xml?displayProperty=nameWithType> 中的其他类（例如 <xref:System.Xml.XmlReader>、<xref:System.Xml.XmlWriter> 和 <xref:System.Xml.Xsl.XslCompiledTransform>）进行互操作。  
  
本主题描述 <xref:System.Xml.Linq.XElement> 类提供的功能。  
  
## <a name="constructing-xml-trees"></a>构造 XML 树  
 可以使用各种方式构造 XML 树，包括以下方式：  
  
- 可以在代码中构造 XML 树。 有关详细信息，请参阅[创建 XML 树 (C#)](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-overview.md)。  
  
- 可以从包括 <xref:System.IO.TextReader>、文本文件或 Web 地址 (URL) 在内的各种源解析 XML。 有关详细信息，请参阅[解析 XML (C#)](../../../../csharp/programming-guide/concepts/linq/how-to-parse-a-string.md)。  
  
- 可以使用 <xref:System.Xml.XmlReader> 来填充树。 有关更多信息，请参见<xref:System.Xml.Linq.XNode.ReadFrom%2A>。  
  
- 如果您有一个可以将内容写入 <xref:System.Xml.XmlWriter> 的模块，则可以使用 <xref:System.Xml.Linq.XContainer.CreateWriter%2A> 方法来创建编写器，将该编写器传递到该模块，然后使用写入 <xref:System.Xml.XmlWriter> 的内容来填充 XML 树。  
  
 但是，创建 XML 树的最常见的方法如下：  
  
```csharp  
XElement contacts =  
    new XElement("Contacts",  
        new XElement("Contact",  
            new XElement("Name", "Patrick Hines"),   
            new XElement("Phone", "206-555-0144"),  
            new XElement("Address",  
                new XElement("Street1", "123 Main St"),  
                new XElement("City", "Mercer Island"),  
                new XElement("State", "WA"),  
                new XElement("Postal", "68042")  
            )  
        )  
    );  
```  
  
 另一个创建 XML 树的十分常用的方法是使用 [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] 查询的结果来填充 XML 树，如下面的示例所示：  
  
```csharp  
XElement srcTree = new XElement("Root",  
    new XElement("Element", 1),  
    new XElement("Element", 2),  
    new XElement("Element", 3),  
    new XElement("Element", 4),  
    new XElement("Element", 5)  
);  
XElement xmlTree = new XElement("Root",  
    new XElement("Child", 1),  
    new XElement("Child", 2),  
    from el in srcTree.Elements()  
    where (int)el > 2  
    select el  
);  
Console.WriteLine(xmlTree);  
```  
  
 该示例产生下面的输出：  
  
```xml  
<Root>  
  <Child>1</Child>  
  <Child>2</Child>  
  <Element>3</Element>  
  <Element>4</Element>  
  <Element>5</Element>  
</Root>  
```  
  
## <a name="serializing-xml-trees"></a>序列化 XML 树  
 可以将 XML 树序列化为 <xref:System.IO.File>、<xref:System.IO.TextWriter> 或 <xref:System.Xml.XmlWriter>。  
  
 有关详细信息，请参阅[序列化 XML 树 (C#)](../../../../csharp/programming-guide/concepts/linq/preserving-white-space-while-serializing.md)。  
  
## <a name="retrieving-xml-data-via-axis-methods"></a>通过轴方法检索 XML 数据  
 可以使用轴方法检索属性、子元素、子代元素和上级元素。 [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] 查询对轴方法进行操作，并提供了多种灵活而有效的方法导航和处理 XML 树。  
  
 有关详细信息，请参阅 [LINQ to XML 轴 (C#)](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-axes-overview.md)。  
  
## <a name="querying-xml-trees"></a>查询 XML 树  
 可以编写从 XML 树提取数据的 [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] 查询。  
  
 有关详细信息，请参阅[查询 XML 树 (C#)](../../../../csharp/programming-guide/concepts/linq/how-to-find-an-element-with-a-specific-attribute.md)。  
  
## <a name="modifying-xml-trees"></a>修改 XML 树  
 可以通过各种方式修改元素，例如更改元素的内容或属性。 还可以从元素的父级移除元素。  
  
 有关详细信息，请参阅[修改 XML 树 (LINQ to XML) (C#)](../../../../csharp/programming-guide/concepts/linq/in-memory-xml-tree-modification-vs-functional-construction-linq-to-xml.md)。  
  
## <a name="see-also"></a>请参阅

- [LINQ to XML 编程概述 (C#)](serializing-to-files-textwriters-and-xmlwriters.md)
