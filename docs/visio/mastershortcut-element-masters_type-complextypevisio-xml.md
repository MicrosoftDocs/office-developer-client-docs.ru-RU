---
title: Элемент MasterShortcut (Мастерс_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Задает ярлык образца, определенный в документе.
ms.openlocfilehash: 03196c6fc1f3424c61bcce406dc050f2d5a73365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341736"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>Элемент MasterShortcut (Мастерс_типе complexType) (' Visio XML ')

Задает ярлык образца, определенный в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Мастершорткут_типе](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Master #. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Мастерс_типе](masters_type-complextypevisio-xml.md) <br/> |Содержит элементы **master** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Икон_типе](icon_type-complextypevisio-xml.md) <br/> |Задает двоичный значок закодированного двоичного расширения MIME (в формате ICO) для **основного** элемента или элемента **MasterShortcut** в документе.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Указывает, выровнен ли текст элемента в окне набора элементов слева, справа или по центру.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Размер значка элемента.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|ИД  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Уникальный идентификатор элемента в родительском элементе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Имя  <br/> |XSD: строка  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа String: XSD.  <br/> |
|NameU  <br/> |XSD: строка  <br/> |необязательный  <br/> |Универсальное имя элемента.  <br/> |Значения типа String: XSD.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Определяет, является ли основной пользователь нестандартным шаблоном.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|Prompt  <br/> |XSD: строка  <br/> |необязательный  <br/> |Строка состояния и приглашение подсказки для элемента.  <br/> |Значения типа String: XSD.  <br/> |
|Шорткуселп  <br/> |XSD: строка  <br/> |необязательный  <br/> |Строка справки для элемента.  <br/> |Значения типа String: XSD.  <br/> |
|Шорткутурл  <br/> |XSD: строка  <br/> |необязательный  <br/> |URL-адрес элемента **MasterShortcut** .  <br/> |Значения типа String: XSD.  <br/> |
   

