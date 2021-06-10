---
title: Свойство UnderlyingValue (ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6d1618a0cb310c1e564fe18289da6a2d35e91d0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314002"
---
# <a name="underlyingvalue-property-ado"></a>Свойство UnderlyingValue (ADO)


**Область применения**: Access 2013, Office 2013



Указывает текущее значение объекта [Field](field-object-ado.md) в базе данных.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **Variant,** которое указывает значение **Поля.**

## <a name="remarks"></a>Примечания

Чтобы вернуть текущее значение поля из базы данных, используйте свойство **UnderlyingValue.** Значение поля в свойстве **UnderlyingValue** — это значение, которое видно для транзакции и может быть результатом недавнего обновления другой транзакции. Это может отличаться от свойства [OriginalValue,](originalvalue-property-ado.md) которое отражает значение, которое было первоначально возвращено в [Набор записей.](recordset-object-ado.md)

Это похоже на использование метода [Resync,](resync-method-ado.md) но свойство **UnderlyingValue** возвращает только значение для определенного поля из текущей записи. Это то же значение, которое метод [Resync](resync-method-ado.md) использует для замены [свойства Value.](value-property-ado.md)

При использовании этого свойства с **свойством OriginalValue** можно разрешить конфликты, возникающие в результате пакетных обновлений.

## <a name="record"></a>Record

Для [объектов Record](record-object-ado.md) это свойство будет пустым для полей, добавленных до того, как будет [вызвано](update-method-ado.md) обновление.

