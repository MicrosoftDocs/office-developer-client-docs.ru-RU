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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281979"
---
# <a name="absoluteposition-property-ado"></a>Свойство AbsolutePosition (ADO)

**Область применения**: Access 2013, Office 2013

Указывает расположение текущей записи объекта [Recordset.](recordset-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Long** от 1 до количества записей в объекте **Recordset** [(RecordCount)](recordcount-property-ado.md)или возвращает одно из [значений PositionEnum.](positionenum.md)

## <a name="remarks"></a>Примечания

Чтобы установить **свойство AbsolutePosition,** ADO требует, чтобы поставщик OLE DB, который вы используете, реализовал интерфейс IRowsetLocate.

Доступ к свойству **AbsolutePosition** для наборов **записей,** открываемых только вперед или динамическим курсором, вызывает ошибку **adErrFeatureNotAvailable.** С другими типами курсоров правильная позиция возвращается до тех пор, пока поставщик поддерживает интерфейс IRowsetScroll. Если поставщик не поддерживает *интерфейс IRowsetScroll,* свойство настроено **на adPosUnknown**. См. документацию для поставщика, чтобы определить, поддерживает ли он *IRowsetScroll.*

Используйте свойство **AbsolutePosition,** чтобы перейти к записи в зависимости от его расположения в объекте **Recordset** или определить ordinal положение текущей записи. Поставщик должен поддерживать соответствующие функции, чтобы это свойство было доступно.

Как и [свойство AbsolutePage,](absolutepage-property-ado.md) **AbsolutePosition** основан на 1 и равен 1, когда текущая запись является первой записью **в Наборе записей.** Общее количество записей в объекте **Recordset** можно получить из свойства [RecordCount.](recordcount-property-ado.md)

При задании свойства **AbsolutePosition,** даже если оно записано в текущем кэше, ADO перезагружает кэш новой группой записей, начиная с указанной записи. Свойство [CacheSize](cachesize-property-ado.md) определяет размер этой группы.


> [!NOTE]
> Свойство **AbsolutePosition** не следует использовать в качестве номера записи суррогата. Положение данной записи меняется при удалении предыдущей записи. Кроме того, нет уверенности в том, что в случае повторного или повторного открытия объекта **Recordset** у данной записи будет одинаковый **absolutePosition.** Закладки по-прежнему являются рекомендуемой возможностью сохранять и возвращаться в заданную позицию и являются единственным способом позиционирования во всех типах объектов **Recordset.**


