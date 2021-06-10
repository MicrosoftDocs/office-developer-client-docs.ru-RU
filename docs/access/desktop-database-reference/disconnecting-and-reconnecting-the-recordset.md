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

Одна из самых мощных функций, найденных в ADO, — это возможность  открыть  клиентский набор записей из источника данных и отсоединить его от источника данных.  После **отключения Recordset** подключение к источнику данных может быть закрыто, тем самым высвободив ресурсы на сервере, используемом для его обслуживания. Вы можете продолжать просматривать и редактировать данные в **Наборе** записей, пока они отключены, а затем повторно подключены к источнику данных, и отправлять обновления в пакетном режиме.

Чтобы отключить **набор Recordset,** откройте его с помощью курсора **adUseClient,** а затем установите свойство **ActiveConnection,** равное *Nothing.* (Пользователи C++ должны установить **для отключения activeConnection** равный NULL.)

В этой главе  мы будем использовать отключенный набор записей, когда мы обсудим сохранение **Recordset** для  решения сценария, при котором данные в наборе записей будут доступны приложению, пока клиентский компьютер не подключен к сети.

