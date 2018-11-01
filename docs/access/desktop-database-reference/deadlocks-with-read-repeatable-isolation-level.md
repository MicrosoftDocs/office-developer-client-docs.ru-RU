---
title: Взаимоблокировок с уровнем изоляции повторяющегося чтения
TOCTitle: Deadlocks With Read Repeatable Isolation Level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9a5fbf4686fc5b8bffc984b4b483f1ee506eb7dd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882989"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>Взаимоблокировок с уровнем изоляции повторяющегося чтения


**Применимо к**: Access 2013, Office 2013

Если настраиваемый бизнес-объект использует уровень изоляции чтения повторяющихся для доступа к SQL Server и бизнес-объект вызывается одновременно с двумя клиентами, отправьте запрос и обновление в той же транзакции, возможна взаимоблокировка. Служба удаленных данных позволяет один процессы, используемые для времени ожидания для освобождения взаимоблокировки, но обновление завершится с ошибкой для этого клиента.

Используйте свойство динамических**время ожидания команды** [Службы курсора](microsoft-cursor-service-for-ole-db-ado-service-component.md)для изменения продолжительность периода ожидания.

