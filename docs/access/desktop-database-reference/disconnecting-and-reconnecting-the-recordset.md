---
title: Отключение и повторное подключение набора записей
TOCTitle: Disconnecting and Reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 094c68fbf5b62a7a1b3af16b826bf9c2c26a2af4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882422"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="91cca-102">Отключение и повторное подключение набора записей</span><span class="sxs-lookup"><span data-stu-id="91cca-102">Disconnecting and Reconnecting the Recordset</span></span>


<span data-ttu-id="91cca-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91cca-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="91cca-104">Отключение и повторное подключение набора записей</span><span class="sxs-lookup"><span data-stu-id="91cca-104">Disconnecting and Reconnecting the Recordset</span></span>

<span data-ttu-id="91cca-105">Одно из наиболее эффективные функции, доступные в ADO — это возможность открыть со стороны клиента **набора записей** из источника данных и затем *Отключите* **набора записей** из источника данных.</span><span class="sxs-lookup"><span data-stu-id="91cca-105">One of the most powerful features found in ADO is the capability to open a client-side **Recordset** from a data source and then *disconnect* the **Recordset** from the data source.</span></span> <span data-ttu-id="91cca-106">После отключения **записей** подключения к источнику данных можно будет закрыто, тем самым освобождения ресурсов на сервере, используемое для поддержки его.</span><span class="sxs-lookup"><span data-stu-id="91cca-106">Once the **Recordset** has been disconnected, the connection to the data source can be closed, thereby releasing the resources on the server used to maintain it.</span></span> <span data-ttu-id="91cca-107">Можно продолжить просмотр и изменение данных в **набор записей** во время его отключения и последующего повторного подключения к источнику данных и отправка обновлений в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="91cca-107">You can continue to view and edit the data in the **Recordset** while it is disconnected and later reconnect to the data source and send your updates in batch mode.</span></span>

<span data-ttu-id="91cca-108">Чтобы прервать **записей**, откройте его с расположения курсора из **adUseClient**и задайте для свойства **ActiveConnection** значение *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="91cca-108">To disconnect a **Recordset**, open it with a cursor location of **adUseClient**, and then set the **ActiveConnection** property equal to *Nothing*.</span></span> <span data-ttu-id="91cca-109">(C++ пользователи должны задавать **ActiveConnection** равно NULL для отключения.)</span><span class="sxs-lookup"><span data-stu-id="91cca-109">(C++ users should set the **ActiveConnection** equal to NULL to disconnect.)</span></span>

<span data-ttu-id="91cca-110">Мы используем отключенного **набора записей** далее в этой главе при обсуждении хранение **записей** для решения проблемы, в котором нужно обновлять данные в **набор записей** для приложения, пока на клиентском компьютере не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="91cca-110">We will use a disconnected **Recordset** later in this chapter when we discuss **Recordset** persistence to address a scenario in which we need to have the data in a **Recordset** available to an application while the client computer is not connected to a network.</span></span>

