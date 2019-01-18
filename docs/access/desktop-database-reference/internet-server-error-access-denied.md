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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720389"
---
# <a name="internet-server-error-access-denied"></a>Ошибка интернет-сервера: "Отказано в доступе"


**Применимо к**: Access 2013, Office 2013

Если возникнет ошибка, это обычно означает, что Microsoft Internet Information Services (IIS) возвращаются следующие состояния:

HTTP\_состояние\_ЗАПРЕЩЕННЫЕ 401

Убедитесь в том, что каталоги, к которым получают доступ служб IIS, имеют соответствующие разрешения. Служб удаленных рабочих СТОЛОВ обмениваться данными с веб-сервере IIS, выполняющегося в любой из трех режимов проверки подлинности пароля: анонимный доступ, Basic или NT запрос и ответ (называемая встроенная проверка подлинности Windows в Windows 2000). Кроме того веб-сервера должны быть разрешения на компьютере источника данных Если это компьютер с Windows NT и Windows 2000.

