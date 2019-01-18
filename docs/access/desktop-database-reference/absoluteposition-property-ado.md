---
title: Свойство AbsolutePosition (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b5e25e014c6e93d35e3621bb9b5b3c21d5e77f9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702378"
---
# <a name="absoluteposition-property-ado"></a>Свойство AbsolutePosition (ADO)

**Применимо к**: Access 2013, Office 2013

Указывает порядковый номер текущей записи объекта [набора записей](recordset-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение типа **Long** от 1 число записей в объекте **набора записей** ([RecordCount](recordcount-property-ado.md)) либо одно из значений [PositionEnum](positionenum.md) .

## <a name="remarks"></a>Замечания

Чтобы задать свойство **AbsolutePosition** , ADO требует, что поставщика OLE DB, который вы используете реализовать интерфейс IRowsetLocate.

Доступ к **AbsolutePosition** свойство **набора записей** , который был открыт для последовательного доступа или динамический курсор вызывает ошибки **adErrFeatureNotAvailable**. Другие типы курсора надлежащих позициях будут возвращены до тех пор, пока поставщик поддерживает интерфейс IRowsetScroll. Если поставщик поддерживает интерфейс *IRowsetScroll* , свойство имеет значение **adPosUnknown**. Обратитесь к документации для поставщика, чтобы определить, поддерживает ли *IRowsetScroll*.

Используйте свойство **AbsolutePosition** для переноса записей по его порядковый номер в объекте **набора записей** или для определения порядковый номер текущей записи. Поставщик должен поддерживать соответствующие функциональные возможности для этого свойства, чтобы оно было доступно.

Как и свойство [AbsolutePage](absolutepage-property-ado.md) **AbsolutePosition** на основе 1 и имеет значение 1, если текущая запись является первой записи в **набор записей**. Общее число записей в объекте **набора записей** можно получить из свойства [RecordCount](recordcount-property-ado.md) .

Если задать свойство **AbsolutePosition** даже в том случае, если это записи в текущей кэш-памяти, ADO перезагружает кэша с новой группы записей, начиная с записью, указанной. Свойство [CacheSize](cachesize-property-ado.md) определяет размер этой группы.


> [!NOTE]
> Не следует использовать свойство **AbsolutePosition** как номер заменяющего записи. Положение данной записи изменений при удалении предыдущей записи. Нет никакой гарантии, что данной записи будут иметь же **AbsolutePosition** , если опросить или повторном открытии в объект **набора записей** . Закладки по-прежнему не рекомендуемый способ сохранения и возврата в заданной позиции, а также являются единственным способом размещения для всех типов объектов **наборов записей** .


