---
title: 如何：设置 ToolBar 上控件的样式
ms.date: 03/30/2017
helpviewer_keywords:
- styling controls on toolbar [WPF]
- toolbars [WPF]
- customizing controls on toolbar [WPF]
ms.assetid: ba6ae056-d6a9-4c24-90f8-467ab0bc0b1a
ms.openlocfilehash: 90ff02747d762b5853a1f60eb99be574503e27f7
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2019
ms.locfileid: "64640846"
---
# <a name="how-to-style-controls-on-a-toolbar"></a>如何：设置 ToolBar 上控件的样式
<xref:System.Windows.Controls.ToolBar>定义<xref:System.Windows.ResourceKey>对象来指定中的控件的样式<xref:System.Windows.Controls.ToolBar>。  若要设置样式中的控件<xref:System.Windows.Controls.ToolBar>，将`x:key`到样式属性<xref:System.Windows.ResourceKey>中定义<xref:System.Windows.Controls.ToolBar>。  
  
 <xref:System.Windows.Controls.ToolBar>定义了以下<xref:System.Windows.ResourceKey>对象：  
  
- <xref:System.Windows.Controls.ToolBar.ButtonStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.CheckBoxStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.ComboBoxStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.MenuStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.RadioButtonStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.SeparatorStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.TextBoxStyleKey%2A>  
  
- <xref:System.Windows.Controls.ToolBar.ToggleButtonStyleKey%2A>  
  
## <a name="example"></a>示例  
 下面的示例定义内的控件的样式<xref:System.Windows.Controls.ToolBar>。  
  
 [!code-xaml[ToolBar_snip#ToolBarAllStyles](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolBar_snip/CS/pane1.xaml#toolbarallstyles)]  
[!code-xaml[ToolBar_snip#ToolBar](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolBar_snip/CS/pane1.xaml#toolbar)]  
  
## <a name="see-also"></a>请参阅

- [样式设置和模板化](styling-and-templating.md)
