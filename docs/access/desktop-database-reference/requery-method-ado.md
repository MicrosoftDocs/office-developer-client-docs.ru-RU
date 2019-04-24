---
title: Метод reQuery (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dc236d730cf773ec38fe5dd903cb64ca9b594
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306715"
---
# <a name="requery-method-ado"></a>Метод reQuery (ADO)

**Область применения**: Access 2013, Office 2013

Обновляет данные в объекте [Recordset](recordset-object-ado.md) с помощью повторного выполнения запроса, на котором основан объект.

## <a name="syntax"></a>Синтаксис

*набор записей*. *Параметры* запроса

## <a name="parameters"></a>Параметры

|Имя |Описание|
|:----|:----------|
|*Options* |Необязательный атрибут. Битовая маска, содержащая значения [ексекутеоптионенум](executeoptionenum.md) и [коммандтипинум](commandtypeenum.md) , которые влияют на эту операцию.|

> [!NOTE]
> Если *параметру* присвоено значение **адасинцексекуте**, эта операция выполняется асинхронно и при завершении работы будет создано событие [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) .

Значения **ексекутеопененум** для **адексекутенорекордс** или **адексекутестреам** не следует использовать вместе с параметром Requery. ****

## <a name="remarks"></a>Замечания

Используйте метод **reissuing** для обновления всего содержимого объекта **Recordset** из источника данных путем повторного выпуска исходной команды и извлечения данных во второй раз. Вызов этого метода эквивалентен вызову методов [Close](close-method-ado.md) и [Open](open-method-ado-recordset.md) в ходе выполнения. При редактировании текущей записи или добавлении новой записи возникает ошибка.

Пока открыт объект **Recordset** , свойства, определяющие природу курсора ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [maxRecords](maxrecords-property-ado.md)и т. д.), доступны только для чтения. Таким образом, **** метод Requery может обновить только текущий курсор. Чтобы изменить свойства курсора и просмотреть результаты, необходимо использовать метод [Close](close-method-ado.md) , чтобы свойства стали доступны для чтения и записи. Затем можно изменить параметры свойства и вызвать метод [Open](open-method-ado-recordset.md) для повторного открытия курсора.

