---
title: 如何：在 Windows 窗体上定位控件
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- Location
- Location.Y
- Location.X
helpviewer_keywords:
- controls [Windows Forms]
- controls [Windows Forms], moving
- snaplines
- controls [Windows Forms], positioning
ms.assetid: 4693977e-34a4-4f19-8221-68c3120c2b2b
ms.openlocfilehash: 241edbe60c327493c9123c6cf7bdc19b7ba2b724
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211655"
---
# <a name="how-to-position-controls-on-windows-forms"></a>如何：在 Windows 窗体上定位控件

若要定位控件，在 Visual Studio 中使用 Windows 窗体设计器或指定<xref:System.Windows.Forms.Control.Location%2A>属性。

## <a name="position-a-control-on-the-design-surface-of-the-windows-forms-designer"></a>Windows 窗体设计器在设计图面上的将控件放

在 Visual Studio 中，将控件拖动到用鼠标的适当位置。

> [!NOTE]
> 选择控件并移动它带有箭头键以更精确地放置。 此外，*对齐线*帮助您在放置在窗体上精确的控制。 有关详细信息，请参见[演练：在 Windows 上排列控件窗体使用对齐线](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)。

## <a name="position-a-control-using-the-properties-window"></a>定位控件的使用属性窗口

1. 在 Visual Studio 中，单击你想要定位的控件。

2. 在中**属性**窗口中，类型值<xref:System.Windows.Forms.Control.Location%2A>属性，由逗号分隔，以放置在其容器内的控件。

     第一个数字 (X) 是容器的从左边框; 的距离第二个数字 (Y) 是上边界的容器区域中，以像素为单位的距离。

    > [!NOTE]
    > 您可以展开<xref:System.Windows.Forms.Control.Location%2A>属性键入**X**并**Y**单独值。

## <a name="position-a-control-programmatically"></a>以编程方式定位控件

1. 设置<xref:System.Windows.Forms.Control.Location%2A>到控件属性<xref:System.Drawing.Point>。

    ```vb
    Button1.Location = New Point(100, 100)
    ```

    ```csharp
    button1.Location = new Point(100, 100);
    ```

    ```cpp
    button1->Location = Point(100, 100);
    ```

2. 更改控件的位置的 X 坐标使用<xref:System.Windows.Forms.Control.Left%2A>子属性。

    ```vb
    Button1.Left = 300
    ```

    ```csharp
    button1.Left = 300;
    ```

    ```cpp
    button1->Left = 300;
    ```

## <a name="increment-a-controls-location-programmatically"></a>以编程方式递增控件的位置

设置<xref:System.Windows.Forms.Control.Left%2A>子属性要递增的控件的 X 坐标。

```vb
Button1.Left += 200
```

```csharp
button1.Left += 200;
```

```cpp
button1->Left += 200;
```

> [!NOTE]
> 使用<xref:System.Windows.Forms.Control.Location%2A>要设置控件的 X 和 Y 属性将同时定位。 若要单独设置位置，请使用控件的<xref:System.Windows.Forms.Control.Left%2A>(**X**) 或<xref:System.Windows.Forms.Control.Top%2A>(**Y**) 子属性。 不要尝试隐式设置的 X 和 Y 坐标<xref:System.Drawing.Point>结构，它表示该按钮的位置，因为此结构包含按钮的坐标的副本。

## <a name="see-also"></a>请参阅

- [Windows 窗体控件](index.md)
- [演练：使用对齐线的 Windows 窗体上排列控件](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
- [演练：使用 TableLayoutPanel 的 Windows 窗体上排列控件](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [演练：使用 FlowLayoutPanel 的 Windows 窗体上排列控件](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)
- [在 Windows 窗体上排列控件](arranging-controls-on-windows-forms.md)
- [标记各个 Windows 窗体控件并创建它们的快捷键](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [在 Windows 窗体上使用的控件](controls-to-use-on-windows-forms.md)
- [按功能列出的 Windows 窗体控件](windows-forms-controls-by-function.md)
- [如何：设置 Windows 窗体的屏幕位置](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/52aha046(v=vs.100))
