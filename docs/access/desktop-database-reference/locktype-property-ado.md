---
title: Свойство LockType (ADO)
TOCTitle: LockType property (ADO)
ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15)
ms:contentKeyID: 48543589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d12946a90d61a941bf5ef7d479970c8c96e074f9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712479"
---
# <a name="locktype-property-ado"></a>Свойство LockType (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает тип блокировки записей во время редактирования.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [LockTypeEnum](locktypeenum.md) . Значение по умолчанию — **adLockReadOnly**.

## <a name="remarks"></a>Замечания

Присвойте свойству **LockType для** перед открытием [набора записей](recordset-object-ado.md) , чтобы указать, какой блокировки поставщика следует использовать при открытии его. Чтение свойства для возвращения типа блокировки используется open объекта **набора записей** .

Поставщики могут не поддерживать все типы блокировки. Если поставщик не поддерживает запрошенный **LockType для** параметра, он будет заменить другой тип блокировки. Чтобы определить фактический блокировки функциональные возможности, доступные в объекте **набора записей** , используйте метод [поддерживает](supports-method-ado.md) с **adUpdate** и **adUpdateBatch**.

Параметр **adLockPessimistic** не поддерживается, если свойство [CursorLocation](cursorlocation-property-ado.md) имеет значение **adUseClient**. Если задано значение не поддерживается, сообщение об ошибке не приведет к; ближайший поддерживаемый **LockType для** будет использоваться.

Свойство **LockType для** чтения и записи при выполняется **записей** закрытой и только для чтения при открытии.

**Службы удаленных данных об использовании** При использовании в объект набора записей со стороны клиента, свойство **LockType для** может устанавливаться только для **adLockBatchOptimistic**.

