---
title: 'Ошибка сервера Интернета: Отказано в доступе'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 885bdc14e5d5d346a17e018a509acf5b6c52108d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944881"
---
# <a name="internet-server-error-access-denied"></a>Ошибка сервера Интернета: Отказано в доступе


**Применимо к**: Access 2013, Office 2013

Если возникнет ошибка, это обычно означает, что Microsoft Internet Information Services (IIS) возвращаются следующие состояния:

HTTP\_состояние\_ЗАПРЕЩЕННЫЕ 401

Убедитесь в том, что каталоги, к которым получают доступ служб IIS, имеют соответствующие разрешения. Служб удаленных рабочих СТОЛОВ обмениваться данными с веб-сервере IIS, выполняющегося в любой из трех режимов проверки подлинности пароля: анонимный доступ, Basic или NT запрос и ответ (называемая встроенная проверка подлинности Windows в Windows 2000). Кроме того веб-сервера должны быть разрешения на компьютере источника данных Если это компьютер с Windows NT и Windows 2000.

