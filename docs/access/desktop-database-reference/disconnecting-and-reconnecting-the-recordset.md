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
# <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="89315-102">Отключение и повторное подключение набора записей</span><span class="sxs-lookup"><span data-stu-id="89315-102">Disconnecting and reconnecting the Recordset</span></span>


<span data-ttu-id="89315-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89315-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="89315-104">Disconnecting and Reconnecting the Recordset</span><span class="sxs-lookup"><span data-stu-id="89315-104">Disconnecting and Reconnecting the Recordset</span></span>

<span data-ttu-id="89315-105">Одна из самых мощных функций ADO — возможность открыть  клиентский набор записей  из источника данных, а затем отключить набор **записей** от источника данных.</span><span class="sxs-lookup"><span data-stu-id="89315-105">One of the most powerful features found in ADO is the capability to open a client-side **Recordset** from a data source and then *disconnect* the **Recordset** from the data source.</span></span> <span data-ttu-id="89315-106">После **отключения recordset** подключение к источнику данных можно закрыть, тем самым освободив ресурсы на сервере, используемом для его обслуживания.</span><span class="sxs-lookup"><span data-stu-id="89315-106">Once the **Recordset** has been disconnected, the connection to the data source can be closed, thereby releasing the resources on the server used to maintain it.</span></span> <span data-ttu-id="89315-107">Вы можете продолжать просматривать и редактировать данные в наборе **записей,** когда он отключен, а затем повторно подключиться к источнику данных и отправить обновления в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="89315-107">You can continue to view and edit the data in the **Recordset** while it is disconnected and later reconnect to the data source and send your updates in batch mode.</span></span>

<span data-ttu-id="89315-108">Чтобы отключить **набор записей,** откройте его с помощью курсора **adUseClient,** а затем задайте для свойства **ActiveConnection** свойство *Nothing.*</span><span class="sxs-lookup"><span data-stu-id="89315-108">To disconnect a **Recordset**, open it with a cursor location of **adUseClient**, and then set the **ActiveConnection** property equal to *Nothing*.</span></span> <span data-ttu-id="89315-109">(Для отключения пользователям C++ следует установить **для ActiveConnection** nULL.)</span><span class="sxs-lookup"><span data-stu-id="89315-109">(C++ users should set the **ActiveConnection** equal to NULL to disconnect.)</span></span>

<span data-ttu-id="89315-110">Мы будем использовать  отключенный набор записей далее в этой главе при обсуждении сохраняемости  наборов записей для решения сценария, в котором данные в наборе записей должны быть доступны приложению, когда клиентский компьютер не подключен к сети. </span><span class="sxs-lookup"><span data-stu-id="89315-110">We will use a disconnected **Recordset** later in this chapter when we discuss **Recordset** persistence to address a scenario in which we need to have the data in a **Recordset** available to an application while the client computer is not connected to a network.</span></span>

