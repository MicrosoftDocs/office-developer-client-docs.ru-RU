---
title: Свойство Field.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95c2776e04497a1ac7f645659c7acc5d9eee2a63
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715965"
---
# <a name="fieldoriginalvalue-property-dao"></a>Свойство Field.OriginalValue (DAO)


**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . OriginalValue

*выражение* Переменная, которая представляет собой объект- **поля** .

## <a name="remarks"></a>Замечания

Во время обновления оптимистичный пакета конфликт может возникнуть, где другой клиент изменяет тем же полем и запишите между время первого клиент получает данные и попытку обновления первого клиента. Свойство **OriginalValue** содержит значение поля во время начала последнего пакета **обновления** . Если это значение не соответствует значению фактически в базе данных, когда пакет **обновления** пытается выполнить запись в базу данных, происходит конфликт. В этом случае будет доступен через свойство **[VisibleValue](field-visiblevalue-property-dao.md)** новое значение в базе данных.

