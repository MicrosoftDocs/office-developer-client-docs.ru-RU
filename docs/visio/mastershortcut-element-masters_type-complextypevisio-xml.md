---
title: Элемент MasterShortcut (Masters_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Задает ярлыка образца, определенным в документе.
ms.openlocfilehash: be3e7d207e58d8c249598a7e156356d4f9e61849
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814212"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>Элемент MasterShortcut (Masters_Type complexType) ('Visio XML»)

Задает ярлыка образца, определенным в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |главные # .xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Образцы](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Содержит **главные** элементы для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Указывает, что кодировке MIME (Multipurpose Internet Mail Extensions) двоичные значок (в формате .ico) для **главной** или **MasterShortcut** элемент в документе.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |XSD:unsignedShort  <br/> |необязательный  <br/> |Задает текст элемента в окне набор элементов выравнивания левой, правой, или центра обработки.  <br/> |Значения типа xsd:unsignedShort.  <br/> |
|IconSize  <br/> |XSD:unsignedShort  <br/> |необязательный  <br/> |Размер значка элемента.  <br/> |Значения типа xsd:unsignedShort.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Уникальный идентификатор элемента в рамках родительского элемента.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Имя  <br/> |XSD:String  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |XSD:String  <br/> |необязательный  <br/> |Универсальные имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|PatternFlags  <br/> |XSD:unsignedShort  <br/> |необязательный  <br/> |Определяет, будет ли шаблон ведет себя как пользовательский шаблон.  <br/> |Значения типа xsd:unsignedShort.  <br/> |
|Запрос  <br/> |XSD:String  <br/> |необязательный  <br/> |Строка состояния и средство запроса подсказки для элемента.  <br/> |Значения типа xsd:string.  <br/> |
|ShortcutHelp  <br/> |XSD:String  <br/> |необязательный  <br/> |Строка справки для элемента.  <br/> |Значения типа xsd:string.  <br/> |
|ShortcutURL  <br/> |XSD:String  <br/> |необязательный  <br/> |URL-адрес элемента **MasterShortcut** .  <br/> |Значения типа xsd:string.  <br/> |
   

