---
title: Взаимоблокировок с уровнем изоляции чтения повторяющихся
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e742a9157c3f2f26d70351fc05afa35472654af9
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944329"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>Взаимоблокировок с уровнем изоляции чтения повторяющихся


**Применимо к**: Access 2013, Office 2013

Если настраиваемый бизнес-объект использует уровень изоляции чтения повторяющихся для доступа к SQL Server и бизнес-объект вызывается одновременно с двумя клиентами, отправьте запрос и обновление в той же транзакции, возможна взаимоблокировка. Служба удаленных данных позволяет один процессы, используемые для времени ожидания для освобождения взаимоблокировки, но обновление завершится с ошибкой для этого клиента.

Используйте свойство динамических**время ожидания команды** [Службы курсора](microsoft-cursor-service-for-ole-db-ado-service-component.md)для изменения продолжительность периода ожидания.

