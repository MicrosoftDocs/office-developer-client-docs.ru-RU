---
title: Повторный запрос метод (ADO)
TOCTitle: Requery Method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be8cbda9e185b3e0b28717e7216f3ff6bea5238c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876129"
---
# <a name="requery-method-ado"></a>Повторный запрос метод (ADO)


**Применимо к**: Access 2013, Office 2013



Обновляет данные в объект [набора записей](recordset-object-ado.md) , повторное выполнение запросов, на котором основан объект.

## <a name="syntax"></a>Синтаксис

*набор записей*. Обновление *параметров*

## <a name="parameter"></a>Параметр

  - *Варианты*

  - Необязательный параметр. Битовая маска, которая содержит значения [ExecuteOptionEnum](executeoptionenum.md) и [CommandTypeEnum](commandtypeenum.md) влияния на этой операции.


> [!NOTE]
> <P>Если <EM>Параметры</EM> <STRONG>adAsyncExecute</STRONG>, эта операция выполняется асинхронно и события <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> будет выдается, когда она завершается.</P>



Значения **ExecuteOpenEnum** **adExecuteNoRecords** или **adExecuteStream** не должен использоваться с **повторный запрос**.

## <a name="remarks"></a>Замечания

Используйте метод **повторный запрос** для обновления все содержимое объекта **набора записей** из источника данных путем получения исходного команды и извлечение данных еще раз. Вызов данного метода эквивалентен вызову метода [Close](close-method-ado.md) и [открытия](open-method-ado-recordset.md) последовательно. Если вы изменяете текущей записи или добавлять новую запись, возникает ошибка.

Когда открыт объекта **набора записей** , свойства, которые определяют характер курсор ([CursorType](cursortype-property-ado.md), [LockType для](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md)и т. д.) доступны только для чтения. Таким образом метод **повторный запрос** можно только обновить курсора. Чтобы изменить свойства курсора и просмотреть результаты, необходимо использовать метод [Close](close-method-ado.md) , чтобы свойства становятся чтение и запись еще раз. Затем можно изменить значения свойств и вызвать метод [Open](open-method-ado-recordset.md) , чтобы снова открыть курсор.

