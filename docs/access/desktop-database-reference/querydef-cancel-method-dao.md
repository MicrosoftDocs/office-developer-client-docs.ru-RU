---
title: Метод QueryDef. Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 56a4ba804dba25eb0b4722bcf5396229ee003f43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301122"
---
# <a name="querydefcancel-method-dao"></a>Метод QueryDef. Cancel (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . Отмена

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Замечания

Используйте метод **Cancel** для завершения выполнения асинхронного вызова метода **EXECUTE** или **OpenConnection** (то есть метод вызывается с помощью параметра дбрунасинк). **Отмена** возвращает ошибку времени выполнения, если дбрунасинк не использовался в методе, который вы пытаетесь завершить.

