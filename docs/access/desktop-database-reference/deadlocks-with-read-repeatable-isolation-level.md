---
title: Тупики с уровнем повторяемой изоляции для чтения
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c3e38f6054e6548dfc14d30ce6ec89dcb2e4b01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294178"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>Тупики с уровнем повторяемой изоляции для чтения


**Область применения**: Access 2013, Office 2013

Если настраиваемый бизнес-объект использует уровень изоляции, который можно повторить, чтобы получить доступ к SQL Server, и бизнес-объект одновременно вызван двумя клиентами, которые отправляют запрос и обновляются в одной транзакции, возможна затор. Служба удаленных данных предназначена для того, чтобы позволить одному из процессов выйти из тупика, но обновление не удастся для этого клиента.

Динамическое свойство Time **Out** службы [Cursor](microsoft-cursor-service-for-ole-db-ado-service-component.md)для изменения длины времени.

