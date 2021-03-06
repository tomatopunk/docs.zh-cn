---
title: 如何：使用系统字体键
ms.date: 03/30/2017
helpviewer_keywords:
- resource keys [WPF], SystemFonts class
ms.assetid: 036ebea7-5677-4f60-8ba4-56c9f9d9b8bd
ms.openlocfilehash: e924f4c14d98380d9f4c0defe27d9f98c3293114
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2019
ms.locfileid: "62001606"
---
# <a name="how-to-use-system-fonts-keys"></a>如何：使用系统字体键
系统资源将多个系统规格以资源的形式公开，以帮助开发人员创建与系统设置一致的视觉效果。 <xref:System.Windows.SystemFonts> 是一个类，包含系统字体值和绑定到这些值的系统字体资源 — 例如，<xref:System.Windows.SystemFonts.CaptionFontFamily%2A>和<xref:System.Windows.SystemFonts.CaptionFontFamilyKey%2A>。  
  
 系统字体规格可用作静态或动态资源。 如果希望字体规格在应用程序运行时自动更新，请使用动态资源；否则，请使用静态资源。  
  
> [!NOTE]
>  动态资源具有关键字*密钥*追加到属性名称。  
  
 以下示例演示如何访问和使用系统字体动态资源来设计按钮样式或自定义按钮。 这[!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]的示例创建分配的按钮样式<xref:System.Windows.SystemFonts>至一个按钮的值。  
  
## <a name="example"></a>示例  
 [!code-xaml[SystemRes_snip#FontDynamicResources](~/samples/snippets/csharp/VS_Snippets_Wpf/SystemRes_snip/CSharp/MyApp.xaml#fontdynamicresources)]  
  
## <a name="see-also"></a>请参阅

- [使用系统画笔绘制区域](../graphics-multimedia/how-to-paint-an-area-with-a-system-brush.md)
- [使用 SystemParameters](how-to-use-systemparameters.md)
- [使用 SystemFonts](how-to-use-systemfonts.md)
