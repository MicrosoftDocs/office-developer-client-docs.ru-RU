---
title: AbsolutePosition Property (ADO)
TOCTitle: AbsolutePosition Property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3258ffcab87b16e4931c9881a8e8d1cd2143262f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482709"
---
# <a name="absoluteposition-property-ado"></a>AbsolutePosition Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает порядковый номер текущей записи объекта [набора записей](recordset-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение типа **Long** от 1 число записей в объекте **набора записей** ([RecordCount](recordcount-property-ado.md)) либо одно из значений [PositionEnum](positionenum.md) .

## <a name="remarks"></a>Замечания

Чтобы задать свойство **AbsolutePosition** , ADO требует, что поставщика OLE DB, который вы используете реализовать интерфейс IRowsetLocate.

Доступ к **AbsolutePosition** свойство **набора записей** , который был открыт для последовательного доступа или динамический курсор вызывает ошибки **adErrFeatureNotAvailable**. Другие типы курсора надлежащих позициях будут возвращены до тех пор, пока поставщик поддерживает интерфейс IRowsetScroll. Если поставщик поддерживает интерфейс *IRowsetScroll* , свойство имеет значение **adPosUnknown**. Обратитесь к документации для поставщика, чтобы определить, поддерживает ли *IRowsetScroll*.

Используйте свойство **AbsolutePosition** для переноса записей по его порядковый номер в объекте **набора записей** или для определения порядковый номер текущей записи. Поставщик должен поддерживать соответствующие функциональные возможности для этого свойства, чтобы оно было доступно.

Как и свойство [AbsolutePage](absolutepage-property-ado.md) **AbsolutePosition** на основе 1 и имеет значение 1, если текущая запись является первой записи в **набор записей**. Общее число записей в объекте **набора записей** можно получить из свойства [RecordCount](recordcount-property-ado.md) .

Если задать свойство **AbsolutePosition** даже в том случае, если это записи в текущей кэш-памяти, ADO перезагружает кэша с новой группы записей, начиная с указанной записи. Свойство [CacheSize](cachesize-property-ado.md) определяет размер этой группы.


> [!NOTE]
> <P>Не следует использовать свойство <STRONG>AbsolutePosition</STRONG> как номер заменяющего записи. Положение данной записи изменений при удалении предыдущей записи. Нет никакой гарантии, что данной записи будут иметь же <STRONG>AbsolutePosition</STRONG> , если опросить или повторном открытии в объект <STRONG>набора записей</STRONG> . Закладки будут по-прежнему рекомендуемый способ сохранения и возврата в заданной позиции и являются единственным способом размещения для всех типов объектов <STRONG>наборов записей</STRONG> .</P>


