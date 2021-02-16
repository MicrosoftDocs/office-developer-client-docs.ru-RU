---
title: Элемент DocumentSheet (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Указывает структуру таблицы документов.
ms.openlocfilehash: 279fca457163d5bcbdda885c11c589bfcde0baa9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540044"
---
# <a name="documentsheet-element-visiodocument_type-complextype-visio-xml"></a>Элемент DocumentSheet (VisioDocument_Type complexType) (Visio XML)

Указывает структуру таблицы документов.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Корневой элемент документа Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Указывает ячейку в документе.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Описывает, было ли имя настроено пользователем.  <br/> |Значения типа xsd:Boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Описывает, было ли универсальное имя настроено пользователем.  <br/> |Значения типа xsd:Boolean.  <br/> |
|Имя  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает зависят от языка имя таблицы документов.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает независимое от языка имя таблицы документов.  <br/> |Значения типа xsd:string.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |необязательный  <br/> |Необязательный атрибут типа string. GUID (глобальный уникальный идентификатор), определяющий фигуру.  <br/> |Значения типа xsd:string.  <br/> |
   

