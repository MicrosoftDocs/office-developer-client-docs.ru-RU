---
title: Элемент HeaderFooterFont (HeaderFooter_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Задает шрифт, используемый для текста верхнего и нижнего колонтитулов.
ms.openlocfilehash: b87ba96d551bf943dd330aa428f2c943c9d29269
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541087"
---
# <a name="headerfooterfont-element-headerfooter_type-complextype-visio-xml"></a>Элемент HeaderFooterFont (HeaderFooter_Type complexType) (XML для Visio)

Задает шрифт, используемый для текста верхнего и нижнего колонтитулов.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Содержит элементы для верхнего и нижнего колонтитулов документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> |Задает кодировку шрифта. Эквивалентно полю Логфонтлфчарсет GDI.  <br/> |Значения типа XSD: Унсигнедбите.  <br/> |
|клиппреЦисион  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> |Задает точность отсечения шрифта. Эквивалентно полю ЛогфонтлфклиппреЦисион GDI.  <br/> |Значения типа XSD: Унсигнедбите.  <br/> |
|Последовательное преобразование  <br/> |XSD: int  <br/> |необязательный  <br/> |Задает атрибут экранирования шрифта. Эквивалентно полю Логфонтлфескапемент GDI.  <br/> |Значения типа XSD: int.  <br/> |
|фаценаме  <br/> |XSD: строка  <br/> |необязательный  <br/> |Содержит сведения о шрифте.  <br/> |Значения типа String: XSD.  <br/> |
|Height  <br/> |XSD: int  <br/> |необязательный  <br/> |Задает высоту фигуры в единицах документа.  <br/> |Значения типа XSD: int.  <br/> |
|Курсив  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> |Указывает, является ли шрифт курсивом. Эквивалентно полю Логфонтлфиталик GDI.  <br/> |Значения типа XSD: Унсигнедбите.  <br/> |
|Вводное обучение  <br/> |XSD: int  <br/> |необязательный  <br/> |Указывает ориентацию шрифта. Эквивалентно полю Логфонтлфориентатион GDI.  <br/> |Значения типа XSD: int.  <br/> |
|Точность  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> |Задает атрибут точности вывода шрифта. Эквивалентно полю ЛогфонтлфаутпреЦисион GDI.  <br/> |Значения типа XSD: Унсигнедбите.  <br/> |
|PitchAndFamily  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> |Указывает шаг и семейство шрифта. Эквивалентно полю Логфонтлфпитчандфамили GDI.  <br/> |Значения типа XSD: Унсигнедбите.  <br/> |
|Качество  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> |Задает качество вывода шрифта. Эквивалентно полю Логфонтлфкуалити GDI.  <br/> |Значения типа XSD: Унсигнедбите.  <br/> |
|Зачеркнутый  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> |Указывает, является ли шрифт зачеркиванием. Эквивалентно полю Логфонтлфстрикеаут GDI.  <br/> |Значения типа XSD: Унсигнедбите.  <br/> |
|Подчеркнутый  <br/> |XSD: Унсигнедбите  <br/> |необязательный  <br/> |Указывает, является ли шрифт подчеркиванием. Эквивалентно полю Логфонтлфундерлине GDI.  <br/> |Значения типа XSD: Унсигнедбите.  <br/> |
|Насыщенность  <br/> |XSD: int  <br/> |необязательный  <br/> |Задает толщину шрифта. Эквивалентно полю Логфонтлфвеигхт GDI.  <br/> |Значения типа XSD: int.  <br/> |
|Width  <br/> |XSD: int  <br/> |необязательный  <br/> |Содержит ширину связанной фигуры в единицах документа.  <br/> |Значения типа XSD: int.  <br/> |
   

