---
title: Field.OriginalValue Property (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ead15a227ccd3ff7d77796aea4d23d776652be86
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873070"
---
# <a name="fieldoriginalvalue-property-dao"></a>Field.OriginalValue Property (DAO)


**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . OriginalValue

*выражение* Переменная, которая представляет собой объект- **поля** .

## <a name="remarks"></a>Замечания

Во время обновления оптимистичный пакета конфликт может возникнуть, где другой клиент изменяет тем же полем и запишите между время первого клиент получает данные и попытку обновления первого клиента. Свойство **OriginalValue** содержит значение поля во время начала последнего пакета **обновления** . Если это значение не соответствует значению фактически в базе данных, когда пакет **обновления** пытается выполнить запись в базу данных, происходит конфликт. В этом случае будет доступен через свойство **[VisibleValue](field-visiblevalue-property-dao.md)** новое значение в базе данных.

