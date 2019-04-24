---
title: Свойство IsolationLevel (ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4eb46fa97b831030617916d03557b5bf9af9606d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291151"
---
# <a name="isolationlevel-property-ado"></a>Свойство IsolationLevel (ADO)


**Область применения**: Access 2013, Office 2013

Указывает уровень изоляции для объекта [подключения](connection-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [исолатионлевеленум](isolationlevelenum.md) . Значение по умолчанию — **адксактчаос**.

## <a name="remarks"></a>Замечания

Используйте свойство **IsolationLevel** , чтобы задать уровень изоляции объекта **Connection** . Параметр не вступает в силу до следующего вызова метода [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) . Если уровень изоляции, который вы запрашиваете, недоступен, поставщик может вернуть следующий более высокий уровень изоляции.

Свойство **IsolationLevel** доступно для чтения и записи.

**Использование удаленной службы данных** При использовании для объекта подключения на стороне клиента свойство **IsolationLevel** можно задать только для **адксактунспеЦифиед**.

Так как пользователи работают с отключенными объектами **Recordset** в кэше на стороне клиента, могут возникнуть проблемы с многопользовательской работой. Например, когда два разных пользователя пытаются обновить одну и ту же запись, служба удаленных данных просто позволяет пользователю, который сначала обновляет эту запись, "выиграть". Запрос на обновление второго пользователя завершается с ошибкой.

