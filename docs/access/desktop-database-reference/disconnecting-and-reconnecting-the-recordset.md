---
title: Отключение и повторное подключение набора записей
TOCTitle: Disconnecting and reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1c028a7d867a105f35b4848ecbe95339f5fcd4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293863"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a>Отключение и повторное подключение набора записей


**Область применения**: Access 2013, Office 2013

## <a name="disconnecting-and-reconnecting-the-recordset"></a>Disconnecting and Reconnecting the Recordset

Одна из самых мощных функций ADO — возможность открыть  клиентский набор записей  из источника данных, а затем отключить набор **записей** от источника данных. После **отключения recordset** подключение к источнику данных можно закрыть, тем самым освободив ресурсы на сервере, используемом для его обслуживания. Вы можете продолжать просматривать и редактировать данные в наборе **записей,** когда он отключен, а затем повторно подключиться к источнику данных и отправить обновления в пакетном режиме.

Чтобы отключить **набор записей,** откройте его с помощью курсора **adUseClient,** а затем задайте для свойства **ActiveConnection** свойство *Nothing.* (Для отключения пользователям C++ следует установить **для ActiveConnection** nULL.)

Мы будем использовать  отключенный набор записей далее в этой главе при обсуждении сохраняемости  наборов записей для решения сценария, в котором данные в наборе записей должны быть доступны приложению, когда клиентский компьютер не подключен к сети. 

