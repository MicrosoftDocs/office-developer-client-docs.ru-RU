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

Указывает номер, который однозначно идентифицирует объект [Error.](error-object-ado.md)

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **Long,** которое может соответствовать одной из констант [ErrorValueEnum.](errorvalueenum.md)

## <a name="remarks"></a>Примечания

Чтобы **определить,** какая ошибка произошла, используйте свойство Number. Значение свойства — уникальный номер, соответствующий условию ошибки.

Коллекция [Ошибок](errors-collection-ado.md) возвращает HRESULT в шестидесятиградном формате (например, 0x80004005) или длинном значении (например, 2147467259). Эти HRESULTs могут быть подняты с помощью основных компонентов, таких как OLE DB или даже сам OLE. Дополнительные сведения об этих номерах см. в главе 16 справочника программиста *OLE DB.*

