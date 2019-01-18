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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700425"
---
# <a name="originalvalue-property-ado"></a>Свойство OriginalValue (ADO)

**Применимо к**: Access 2013, Office 2013

Указывает значение [поля](field-object-ado.md) , которое существовало в записи до внесения изменений.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа Variant** , который представляет значение поля до изменения.

## <a name="remarks"></a>Замечания

Свойство **OriginalValue** возвращает исходное значение поля для поля из текущей записи.

В *режиме немедленное обновление* (где поставщик записывает изменения к базовому источнику данных после вызова метода [обновления](update-method-ado.md) ) это свойство **OriginalValue** возвращает значение поля, существовавшего до внесения изменений (то есть, поскольку Последнее **обновление** вызова метода). Это то же значение, метод [CancelUpdate](cancelupdate-method-ado.md) используется для замены свойства [Value](value-property-ado.md) .

В *пакетном режиме обновления* (в котором поставщик кэширует несколько изменений и записывает их в источнике данных только при вызове метода [UpdateBatch](updatebatch-method-ado.md) ) это свойство **OriginalValue** возвращает значение поля, существовавшего до какие-либо изменяет (то есть, с момента последнего метода **UpdateBatch** звонков). Это то же значение, метод [CancelBatch](cancelbatch-method-ado.md) используется для замены свойства **Value** . При использовании этого свойства с помощью свойства [UnderlyingValue](underlyingvalue-property-ado.md) можно разрешения конфликтов с помощью пакета обновления.

## <a name="record"></a>Record

Для [записи](record-object-ado.md) объектов **OriginalValue** свойство будет пустым для полей, добавлены, прежде чем будет вызван метод [Update](update-method-ado.md) .

