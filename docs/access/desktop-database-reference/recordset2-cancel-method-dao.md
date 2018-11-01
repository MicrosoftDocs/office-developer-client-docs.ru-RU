---
title: Recordset2.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5df46c36ff28bae1e48dfc8dc77443f707fc3e0a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877536"
---
# <a name="recordset2cancel-method-dao"></a>Recordset2.Cancel Method (DAO)


**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . Отмена

*выражение* Выражение, возвращающее объект **Recordset2** .

## <a name="remarks"></a>Замечания

Использование метода **Cancel** для завершения выполнения асинхронного вызова метода **Execute** или **OpenConnection** (то есть, метод был вызван с параметром dbRunAsync). **Отменить** возвращает ошибку времени выполнения, если в метод, который вы пытаетесь прерывания не используется dbRunAsync.

