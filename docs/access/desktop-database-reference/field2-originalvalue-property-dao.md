---
title: Свойство Field2.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 10fed55e-c938-2ae6-8fd2-996745a63da3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845353(v=office.15)
ms:contentKeyID: 48543306
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101183
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e3da5f7438ae83010c6ecc109dccf5d7a8eb9ef
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726136"
---
# <a name="field2originalvalue-property-dao"></a>Свойство Field2.OriginalValue (DAO)


**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . OriginalValue

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Замечания

Во время обновления оптимистичный пакета конфликт может возникнуть, где другой клиент изменяет тем же полем и запишите между время первого клиент получает данные и попытку обновления первого клиента. Свойство **OriginalValue** содержит значение поля во время начала последнего пакета **обновления** . Если это значение не соответствует значению фактически в базе данных, когда пакет **обновления** пытается выполнить запись в базу данных, происходит конфликт. В этом случае будет доступен через свойство **VisibleValue** новое значение в базе данных.

