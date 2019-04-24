---
title: Элемент HeaderFooter (Висиодокумент_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Содержит элементы для верхнего и нижнего колонтитулов документа.
ms.openlocfilehash: eabb19100c4b37a546c0a271cfba5a0c865a7e83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319028"
---
# <a name="headerfooter-element-visiodocumenttype-complextype-visio-xml"></a>Элемент HeaderFooter (Висиодокумент_типе complexType) (' Visio XML ')

Содержит элементы для верхнего и нижнего колонтитулов документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Хеадерфутер_типе](headerfooter_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Висиодокумент](visiodocument-elementvisio-xml.md) <br/> |[Висиодокумент_типе](visiodocument_type-complextypevisio-xml.md) <br/> |Корневой элемент документа Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[FooterCenter](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[Футерцентер_типе](footercenter_type-complextypevisio-xml.md) <br/> |Содержит текстовую строку, которая отображается в центральной части нижнего колонтитула документа.  <br/> |
|[FooterLeft](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[Футерлефт_типе](footerleft_type-complextypevisio-xml.md) <br/> |Содержит текстовую строку, которая отображается в левой части нижнего колонтитула документа.  <br/> |
|[FooterMargin](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[Футермаргин_типе](footermargin_type-complextypevisio-xml.md) <br/> |Задает поля нижнего колонтитула документа.  <br/> |
|[FooterRight](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[Футерригхт_типе](footerright_type-complextypevisio-xml.md) <br/> |Содержит текстовую строку, которая отображается в правой части нижнего колонтитула документа.  <br/> |
|[HeaderCenter](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[Хеадерцентер_типе](headercenter_type-complextypevisio-xml.md) <br/> |Содержит текстовую строку, которая отображается в центральной части заголовка документа.  <br/> |
|[HeaderFooterFont](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[Хеадерфутерфонт_типе](headerfooterfont_type-complextypevisio-xml.md) <br/> |Задает шрифт, используемый для текста верхнего и нижнего колонтитулов.  <br/> |
|[HeaderLeft](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[Хеадерлефт_типе](headerleft_type-complextypevisio-xml.md) <br/> |Содержит текстовую строку, которая отображается в левой части заголовка документа.  <br/> |
|[HeaderMargin](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[Хеадермаргин_типе](headermargin_type-complextypevisio-xml.md) <br/> |Задает поле заголовка документа.  <br/> |
|[HeaderRight](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[Хеадерригхт_типе](headerright_type-complextypevisio-xml.md) <br/> |Содержит текстовую строку, которая отображается в правой части заголовка документа.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|HeaderFooterColor  <br/> |XSD: строка  <br/> |необязательный  <br/> |Значение RGB цвета текста для верхнего и нижнего колонтитулов в шестнадцатеричной нотации; Например, #rrggbb.  <br/> |Значения типа String: XSD.  <br/> |
   

