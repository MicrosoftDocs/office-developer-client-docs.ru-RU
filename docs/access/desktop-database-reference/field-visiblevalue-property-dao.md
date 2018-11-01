---
title: Field.VisibleValue Property (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 462359ca02b4a5724c781da303b13a97c73be388
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871208"
---
# <a name="fieldvisiblevalue-property-dao"></a>Field.VisibleValue Property (DAO)


**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . VisibleValue

*выражение* Переменная, которая представляет собой объект- **поля** .

## <a name="remarks"></a>Замечания

Это свойство содержит значение поля, который в данный момент в базе данных на сервере. Во время обновления оптимистичный пакета конфликт может возникнуть, где второй клиента изменены тем же полем и записи между время первого клиента извлечения данных и попытку обновления первого клиента. В этом случае значение, которое задано второй клиента будет доступен через это свойство.

