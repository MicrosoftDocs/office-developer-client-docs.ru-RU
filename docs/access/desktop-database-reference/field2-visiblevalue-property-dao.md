---
title: Field2.VisibleValue Property (DAO)
TOCTitle: VisibleValue Property
ms:assetid: 1e023a1a-fd49-7570-42bd-2f4c06ac5e5e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845809(v=office.15)
ms:contentKeyID: 48543611
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101184
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9c901045f1f856142a628fb31806610e7d5dce43
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480153"
---
# <a name="field2visiblevalue-property-dao"></a>Field2.VisibleValue Property (DAO)


**Применимо к**: Access 2013 | Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . VisibleValue

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Замечания

Это свойство содержит значение поля, который в данный момент в базе данных на сервере. Во время обновления оптимистичный пакета конфликт может возникнуть, где второй клиента изменены тем же полем и записи между время первого клиента извлечения данных и попытку обновления первого клиента. В этом случае значение, которое задано второй клиента будет доступен через это свойство.

