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

Указывает значение поля, которое [существовало](field-object-ado.md) в записи до внесения каких-либо изменений.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **Variant,** которое представляет значение поля перед любым изменением.

## <a name="remarks"></a>Заметки

Используйте свойство **OriginalValue** для возврата исходного значения поля из текущей записи.

В режиме немедленного обновления *(в* котором поставщик записывает изменения в исходный источник данных после вызова метода [Update)](update-method-ado.md) свойство **OriginalValue** возвращает значение поля, которое существовало до любых изменений (то есть с момента последнего вызова метода **Update).** Это то же значение, которое метод [CancelUpdate](cancelupdate-method-ado.md) использует для замены [свойства Value.](value-property-ado.md)

В режиме пакетного обновления *(в* котором поставщик кэшировать несколько изменений и записывает их в исходный источник данных только при вызове метода [UpdateBatch)](updatebatch-method-ado.md) свойство **OriginalValue** возвращает значение поля, которое существовало до любых изменений (то есть с момента последнего вызова метода **UpdateBatch).** Это то же значение, которое метод [CancelBatch](cancelbatch-method-ado.md) использует для замены **свойства Value.** При использовании этого свойства со [свойством UnderlyingValue](underlyingvalue-property-ado.md) можно устранить конфликты, возникающие в результате пакетных обновлений.

## <a name="record"></a>Record

Для [объектов Record](record-object-ado.md) свойство **OriginalValue** будет пустым для полей, добавленных перед тем, как будет [вызвано обновление.](update-method-ado.md)

