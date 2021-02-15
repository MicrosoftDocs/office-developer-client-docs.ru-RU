---
title: Метод QueryDef.Close (DAO)
TOCTitle: Close Method
ms:assetid: b2b63462-453d-9e2b-0bb3-69a4a7a6ecef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822031(v=office.15)
ms:contentKeyID: 48547179
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052976
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4d50fa52ff4f5d669b062a052bf3e59a28a9e732
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303306"
---
# <a name="querydefclose-method-dao"></a>Метод QueryDef.Close (DAO)


**Область применения**: Access 2013, Office 2013

Закрывает открытый **queryDef.**

## <a name="syntax"></a>Синтаксис

*выражение*.Close

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Примечания

Если объект **QueryDef уже закрыт** при использовании **close,** возникает ошибка во время выполнения.

Альтернатива методу **Close** заключается в присвоении объектной переменной значения **Nothing** (Set dbsTemp = Nothing).

