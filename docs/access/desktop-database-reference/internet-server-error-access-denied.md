---
title: 'Ошибка интернет-сервера: "Отказано в доступе"'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: af823f46653b3ec83950c2e2cfe639b514196b08
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291257"
---
# <a name="internet-server-error-access-denied"></a>Ошибка интернет-сервера: "Отказано в доступе"


**Область применения**: Access 2013, Office 2013

Если вы получите эту ошибку, обычно это означает, что Microsoft IIS (IIS) вернул следующее состояние:

HTTP \_ STATUS \_ DENIED 401

Убедитесь, что каталоги, к которые имеют доступ IIS, имеют соответствующие разрешения. Службы RDS могут взаимодействовать с веб-сервером IIS, работающим в любом из трех режимов проверки подлинности паролем: анонимном, базовом или NT Challenge/Response (называемом встроенной проверкой подлинности Windows в Windows 2000). Кроме того, веб-сервер должен иметь разрешения на доступ к компьютеру источника данных, если это компьютер Windows NT/Windows 2000.

