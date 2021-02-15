---
title: Свойство Field.VisibleValue (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b3e1b6ec6cd34112f0ba1d84101390bbd400f82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292918"
---
# <a name="fieldvisiblevalue-property-dao"></a>Свойство Field.VisibleValue (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение .* VisibleValue

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Примечания

Это свойство содержит значение поля, которое в настоящее время находится в базе данных на сервере. Во время оптимистичного пакетного обновления может возникнуть конфликт, в результате чего второй клиент изменил одно и то же поле и запись между моментом получения данных первым клиентом и первой попыткой обновления клиента. В этом случае значение, которое будет доступно второму набору клиентов, будет доступно через это свойство.

