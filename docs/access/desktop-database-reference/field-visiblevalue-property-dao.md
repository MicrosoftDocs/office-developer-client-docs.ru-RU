---
title: Свойство Field. Висиблевалуе (DAO)
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
# <a name="fieldvisiblevalue-property-dao"></a>Свойство Field. Висиблевалуе (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . Висиблевалуе

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Комментарии

Это свойство содержит значение поля, которое в настоящее время находится в базе данных на сервере. Во время оптимистического пакетного обновления может произойти конфликт, при котором второй клиент изменил то же поле и записывает данные между моментом, когда первый клиент получил данные, и попытка обновления первого клиента. В этом случае значение, которое будет доступно во втором наборе клиентов, будет доступно через это свойство.

