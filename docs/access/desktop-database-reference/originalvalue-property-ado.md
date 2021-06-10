---
title: Свойство OriginalValue (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0724320e1aaa1e7bfd3ceab8cf54afd5921c7425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288184"
---
# <a name="originalvalue-property-ado"></a>Свойство OriginalValue (ADO)

**Область применения**: Access 2013, Office 2013

Указывает значение [поля,](field-object-ado.md) которое существовало в записи до внесения каких-либо изменений.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **Variant,** которое представляет значение поля перед любым изменением.

## <a name="remarks"></a>Примечания

Чтобы вернуть исходное значение поля для поля из текущей записи, используйте свойство **OriginalValue.**

В режиме немедленного обновления (в котором поставщик записывает изменения [](update-method-ado.md) в исходный источник данных после вызова метода Обновления), свойство **OriginalValue** возвращает значение  поля, которое существовало до каких-либо изменений (то есть после последнего вызова метода обновления).  Это то же значение, которое использует метод [CancelUpdate](cancelupdate-method-ado.md) для замены [свойства Value.](value-property-ado.md)

В режиме пакетного обновления *(в* котором поставщик кэшировать несколько изменений и записывает их в исходный источник данных только при вызове метода [UpdateBatch),](updatebatch-method-ado.md) свойство **OriginalValue** возвращает значение поля, которое существовало до каких-либо изменений (то есть после последнего вызова метода **UpdateBatch).** Это то же значение, которое метод [CancelBatch](cancelbatch-method-ado.md) использует для замены **свойства Value.** При использовании этого свойства с [свойством UnderlyingValue](underlyingvalue-property-ado.md) можно разрешить конфликты, возникающие в результате пакетных обновлений.

## <a name="record"></a>Record

Для [объектов Записи](record-object-ado.md) свойство **OriginalValue** будет пустым для полей, добавленных до того, как [будет вызвано](update-method-ado.md) обновление.

