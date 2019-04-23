---
title: Свойство Number (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5eb46d6fbeb677e6d0fe73223d74ae2ea42d368
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288576"
---
# <a name="number-property-ado"></a>Свойство Number (ADO)


**Область применения**: Access 2013, Office 2013

Указывает номер, который уникально идентифицирует объект [Error](error-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает **длинное** значение, которое может соответствовать одной из констант [еррорвалуинум](errorvalueenum.md) .

## <a name="remarks"></a>Замечания

Чтобы определить, какая ошибка возникла, используйте свойство **Number** . Значение свойства — это уникальный номер, соответствующий условию ошибки.

Коллекция [Errors](errors-collection-ado.md) возвращает HRESULT в шестнадцатеричном формате (например, 0x80004005) или длинном значении (например, 2147467259). Эти значения HRESULT могут вызываться с помощью базовых компонентов, таких как OLE DB или даже OLE. Более подробную информацию об этих номерах можно найти в главе 16 *Справочника программиста OLE DB.*

