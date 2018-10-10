---
title: Deadlocks With Read Repeatable Isolation Level
TOCTitle: Deadlocks With Read Repeatable Isolation Level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de936da2772b809199d3890140683afd5ef01659
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480359"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>Deadlocks With Read Repeatable Isolation Level


**Применимо к**: Access 2013 | Office 2013

Если настраиваемый бизнес-объект использует уровень изоляции чтения повторяющихся для доступа к SQL Server и бизнес-объект вызывается одновременно с двумя клиентами, отправьте запрос и обновление в той же транзакции, возможна взаимоблокировка. Служба удаленных данных позволяет один процессы, используемые для времени ожидания для освобождения взаимоблокировки, но обновление завершится с ошибкой для этого клиента.

Используйте свойство динамических**время ожидания команды** [Службы курсора](microsoft-cursor-service-for-ole-db-ado-service-component.md)для изменения продолжительность периода ожидания.

