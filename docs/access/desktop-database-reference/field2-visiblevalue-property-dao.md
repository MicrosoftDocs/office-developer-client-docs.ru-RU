---
title: Свойство field2. Висиблевалуе (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 0161ea66068457b53a9667a6739c3a3a0458c8c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292617"
---
# <a name="field2visiblevalue-property-dao"></a>Свойство field2. Висиблевалуе (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . висиблевалуе

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Примечания

Это свойство содержит значение поля, которое в настоящее время находится в базе данных на сервере. Во время оптимистического пакетного обновления может произойти конфликт, при котором второй клиент изменил то же поле и записывает данные между моментом, когда первый клиент получил данные, и попытка обновления первого клиента. В этом случае значение, которое будет доступно во втором наборе клиентов, будет доступно через это свойство.

