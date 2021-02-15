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

Указывает порядковую позицию текущей записи объекта [Recordset.](recordset-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает  длинное значение от 1 до числа записей в объекте **Recordset** [(RecordCount)](recordcount-property-ado.md)или возвращает одно из [значений PositionEnum.](positionenum.md)

## <a name="remarks"></a>Заметки

Чтобы установить **свойство AbsolutePosition,** ADO требует, чтобы поставщик OLE DB, который вы используете, реализовал интерфейс IRowsetLocate.

При доступе к свойству **AbsolutePosition** объекта **Recordset,** открытого с помощью однонастроенного или динамического курсора, вызывается ошибка **adErrFeatureNotAvailable.** При других типах курсоров возвращается правильное положение, если поставщик поддерживает интерфейс IRowsetScroll. Если поставщик не поддерживает интерфейс *IRowsetScroll,* свойству задается свойство **adPosUnknown.** Чтобы определить, поддерживает ли он *IRowsetScroll, см. документацию по поставщику.*

Используйте свойство **AbsolutePosition** для перемещения в запись на основе его порядкового положения в объекте **Recordset** или для определения порядкового положения текущей записи. Поставщик должен поддерживать соответствующие функции, чтобы это свойство было доступно.

Как и [свойство AbsolutePage,](absolutepage-property-ado.md) **AbsolutePosition** основан на 1 и равен 1, когда текущая запись является первой записью в **наборе записей.** Общее число записей в объекте **Recordset** можно получить из свойства [RecordCount.](recordcount-property-ado.md)

При указании свойства **AbsolutePosition,** даже если оно является записью в текущем кэше, ADO перезагружает кэш новой группой записей, начиная с указанной вами записи. Размер этой группы определяется свойством [CacheSize.](cachesize-property-ado.md)


> [!NOTE]
> Не следует использовать свойство **AbsolutePosition в качестве** заменяемого номера записи. Положение заданной записи изменяется при удалении предыдущей записи. Кроме того, нет гарантий, что для записи будет одинаковый **absolutePosition,** если объект **Recordset** повторно или повторно открыт. Закладки по-прежнему являются рекомендуемой возможностью сохранения и возвращения в заданную позицию и являются единственным способом позиционирования во всех типах объектов **Recordset.**


