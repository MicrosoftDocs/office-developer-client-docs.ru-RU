---
title: Field2.OriginalValue Property (DAO)
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
ms.openlocfilehash: a08612076ba138e5e181eec80bec2350fe27ec86
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483015"
---
# <a name="field2originalvalue-property-dao"></a>Field2.OriginalValue Property (DAO)


**Применимо к**: Access 2013 | Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . OriginalValue

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Замечания

Во время обновления оптимистичный пакета конфликт может возникнуть, где другой клиент изменяет тем же полем и запишите между время первого клиент получает данные и попытку обновления первого клиента. Свойство **OriginalValue** содержит значение поля во время начала последнего пакета **обновления** . Если это значение не соответствует значению фактически в базе данных, когда пакет **обновления** пытается выполнить запись в базу данных, происходит конфликт. В этом случае будет доступен через свойство **VisibleValue** новое значение в базе данных.

