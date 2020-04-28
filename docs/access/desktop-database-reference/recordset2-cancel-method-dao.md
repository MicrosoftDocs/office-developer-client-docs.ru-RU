---
title: Метод Recordset2. Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307415"
---
# <a name="recordset2cancel-method-dao"></a>Метод Recordset2. Cancel (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . Отмена

*Expression (выражение* ) Выражение, возвращающее объект **Recordset2** .

## <a name="remarks"></a>Примечания

Используйте метод **Cancel** для завершения выполнения асинхронного вызова метода **EXECUTE** или **OpenConnection** (то есть метод вызывается с помощью параметра дбрунасинк). **Отмена** возвращает ошибку времени выполнения, если дбрунасинк не использовался в методе, который вы пытаетесь завершить.

