---
title: Элемент Master (Мастерс_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Содержит элементы, определяющие шаблон для документа.
ms.openlocfilehash: f6effa521b7c5ea69d41b6770ee2dbef61af097c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283967"
---
# <a name="master-element-masterstype-complextype-visio-xml"></a>Элемент Master (Мастерс_типе complexType) (' XML ' Visio ')

Содержит элементы, определяющие шаблон для документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Мастер_типе](master_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Главные. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Коннектс_типе](connects_type-complextypevisio-xml.md) <br/> |Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Икон_типе](icon_type-complextypevisio-xml.md) <br/> |Задает двоичный значок закодированного двоичного расширения MIME (в формате ICO) для **основного** элемента или элемента **MasterShortcut** в документе.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Пажешит_типе](pagesheet_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие лист страницы для элемента **Page** или **master** .  <br/> |
|Формы  <br/> |Шапес_типе  <br/> |Содержит коллекцию элементов **Shape** .  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Указывает, выровнен ли текст образца в окне набора элементов слева, справа или по центру.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|BaseID  <br/> |XSD: строка  <br/> |необязательный  <br/> |Глобальный уникальный идентификатор (GUID), идентифицирующий основной в документах.  <br/> |Значения типа String: XSD.  <br/> |
|Скрытый  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, скрыт ли образец в пользовательском интерфейсе.  <br/> |Значения типа XSD: Boolean.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Размер значка элемента.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, создается ли значок автоматически на основе самого основного образца.  <br/> |Значения типа XSD: Boolean.  <br/> |
|ИД  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Уникальный идентификатор элемента в родительском элементе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|MatchByName  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Определяет, как Microsoft Visio определяет, присутствует ли образец документа при удалении экземпляра шаблона на страницу документа.  <br/> |Значения типа XSD: Boolean.  <br/> |
|Имя  <br/> |XSD: строка  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа String: XSD.  <br/> |
|NameU  <br/> |XSD: строка  <br/> |необязательный  <br/> |Универсальное имя элемента.  <br/> |Значения типа String: XSD.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Определяет, является ли основной пользователь нестандартным шаблоном.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|Prompt  <br/> |XSD: строка  <br/> |необязательный  <br/> |Строка состояния и приглашение подсказки для элемента.  <br/> |Значения типа String: XSD.  <br/> |
|UniqueID  <br/> |XSD: строка  <br/> |необязательный  <br/> |Идентификатор GUID, определяющий образец в документе.  <br/> |Значения типа String: XSD.  <br/> |
   

