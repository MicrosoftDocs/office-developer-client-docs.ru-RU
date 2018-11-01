---
title: Свойство UnderlyingValue (ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d91dccb88ff39ad344ffa0e59e7ccdaaa9f1565
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867785"
---
# <a name="underlyingvalue-property-ado"></a>Свойство UnderlyingValue (ADO)


**Применимо к**: Access 2013, Office 2013



Указывает объект [поля](field-object-ado.md) текущим значением в базе данных.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа Variant** , которое указывает значение **поля**.

## <a name="remarks"></a>Замечания

Свойство **UnderlyingValue** возвращает текущее значение поля из базы данных. Значение поля в свойстве **UnderlyingValue** — это значение, которое будет отображаться транзакции и может быть вызвана последнее обновление с другой транзакции. Могут отличаться от свойств [OriginalValue](originalvalue-property-ado.md) , который отражает значение, которое было изначально возвращаемых [записей](recordset-object-ado.md).

Это похоже на использование метода [выполнить повторную синхронизацию](resync-method-ado.md) , но это свойство **UnderlyingValue** возвращает только значение определенного поля из текущей записи. Это то же значение, которое использует метод [выполнить повторную синхронизацию](resync-method-ado.md) для замены свойства [Value](value-property-ado.md) .

При использовании этого свойства с помощью свойства **OriginalValue** можно разрешения конфликтов с помощью пакета обновления.

## <a name="record"></a>Запись

Для [записи](record-object-ado.md) объектов это свойство будет пустым для полей, добавлены, прежде чем будет вызван метод [Update](update-method-ado.md) .

