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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289845"
---
# <a name="locktype-property-ado"></a>Свойство LockType (ADO)


**Область применения**: Access 2013, Office 2013

Указывает тип блокировок, размещенных на записях во время редактирования.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение [LockTypeEnum.](locktypeenum.md) По умолчанию значение **adLockReadOnly**.

## <a name="remarks"></a>Примечания

Установите свойство **LockType** перед открытием [набора записей,](recordset-object-ado.md) чтобы указать, какой тип блокировки должен использовать поставщик при его открытии. Ознакомьтесь с свойством, чтобы вернуть тип блокировки, используемой на открытом объекте **Recordset.**

Поставщики могут поддерживать не все типы блокировки. Если поставщик не может поддерживать запрашиваемую настройку **LockType,** он заменит другой тип блокировки. Чтобы определить фактическую функциональность блокировки, доступную в **объекте Recordset,** используйте метод [Supports](supports-method-ado.md) с **помощью adUpdate** и **adUpdateBatch.**

Параметр **adLockPessimistic** не поддерживается, если свойство [CursorLocation](cursorlocation-property-ado.md) настроено **на adUseClient.** Если установлено неподтверченные значения, то ошибка не приведет; Вместо этого будет использоваться самый близкий поддерживаемый **LockType.**

Свойство **LockType** считыв или записывалось при закрытии **и** только для чтения, когда оно открыто.

**Удаленное использование службы данных** Свойство **LockType,** используемого на клиентском объекте Recordset, может быть задано **только adLockBatchOptimistic.**

