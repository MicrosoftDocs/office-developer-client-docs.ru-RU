---
title: QueryDef.Cancel Method (DAO)
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
ms.openlocfilehash: 17e6c98851aa20a6a094223eeabb68fe40e719d5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480533"
---
# <a name="querydefcancel-method-dao"></a>QueryDef.Cancel Method (DAO)


**Применимо к**: Access 2013 | Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . Отмена

*выражение* Переменная, которая представляет собой объект- **QueryDef** .

## <a name="remarks"></a>Замечания

Использование метода **Cancel** для завершения выполнения асинхронного вызова метода **Execute** или **OpenConnection** (то есть, метод был вызван с параметром dbRunAsync). **Отменить** возвращает ошибку времени выполнения, если в метод, который вы пытаетесь прерывания не используется dbRunAsync.

