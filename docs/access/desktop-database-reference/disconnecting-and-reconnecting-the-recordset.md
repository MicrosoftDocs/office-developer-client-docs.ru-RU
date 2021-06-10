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
# <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="d9451-102">Отключение и повторное подключение набора записей</span><span class="sxs-lookup"><span data-stu-id="d9451-102">Disconnecting and reconnecting the Recordset</span></span>


<span data-ttu-id="d9451-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9451-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="d9451-104">Disconnecting and Reconnecting the Recordset</span><span class="sxs-lookup"><span data-stu-id="d9451-104">Disconnecting and Reconnecting the Recordset</span></span>

<span data-ttu-id="d9451-105">Одна из самых мощных функций, найденных в ADO, — это возможность  открыть  клиентский набор записей из источника данных и отсоединить его от источника данных. </span><span class="sxs-lookup"><span data-stu-id="d9451-105">One of the most powerful features found in ADO is the capability to open a client-side **Recordset** from a data source and then *disconnect* the **Recordset** from the data source.</span></span> <span data-ttu-id="d9451-106">После **отключения Recordset** подключение к источнику данных может быть закрыто, тем самым высвободив ресурсы на сервере, используемом для его обслуживания.</span><span class="sxs-lookup"><span data-stu-id="d9451-106">Once the **Recordset** has been disconnected, the connection to the data source can be closed, thereby releasing the resources on the server used to maintain it.</span></span> <span data-ttu-id="d9451-107">Вы можете продолжать просматривать и редактировать данные в **Наборе** записей, пока они отключены, а затем повторно подключены к источнику данных, и отправлять обновления в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="d9451-107">You can continue to view and edit the data in the **Recordset** while it is disconnected and later reconnect to the data source and send your updates in batch mode.</span></span>

<span data-ttu-id="d9451-108">Чтобы отключить **набор Recordset,** откройте его с помощью курсора **adUseClient,** а затем установите свойство **ActiveConnection,** равное *Nothing.*</span><span class="sxs-lookup"><span data-stu-id="d9451-108">To disconnect a **Recordset**, open it with a cursor location of **adUseClient**, and then set the **ActiveConnection** property equal to *Nothing*.</span></span> <span data-ttu-id="d9451-109">(Пользователи C++ должны установить **для отключения activeConnection** равный NULL.)</span><span class="sxs-lookup"><span data-stu-id="d9451-109">(C++ users should set the **ActiveConnection** equal to NULL to disconnect.)</span></span>

<span data-ttu-id="d9451-110">В этой главе  мы будем использовать отключенный набор записей, когда мы обсудим сохранение **Recordset** для  решения сценария, при котором данные в наборе записей будут доступны приложению, пока клиентский компьютер не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="d9451-110">We will use a disconnected **Recordset** later in this chapter when we discuss **Recordset** persistence to address a scenario in which we need to have the data in a **Recordset** available to an application while the client computer is not connected to a network.</span></span>

