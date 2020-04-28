---
title: Минимизация места, занимаемого файлом журнала
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da4bf7c9c30d3b9b37e2835ddeeeab2b2ed8a2c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288878"
---
# <a name="minimizing-log-file-space-usage"></a><span data-ttu-id="28fbb-102">Минимизация места, занимаемого файлом журнала</span><span class="sxs-lookup"><span data-stu-id="28fbb-102">Minimizing log file space usage</span></span>

<span data-ttu-id="28fbb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28fbb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28fbb-104">Файл журнала может быстро заполняться (таким образом приостановить работу сервера), если в базе данных SQL Server имеется большой объем действий.</span><span class="sxs-lookup"><span data-stu-id="28fbb-104">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database.</span></span> <span data-ttu-id="28fbb-105">Можно установить для файла журнала **усечение на контрольной точке** , чтобы значительно увеличить срок жизни файла журнала для базы данных.</span><span class="sxs-lookup"><span data-stu-id="28fbb-105">You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span></span>

<span data-ttu-id="28fbb-106">**Включение усечения для контрольной точки в Microsoft SQL Server 6,5**</span><span class="sxs-lookup"><span data-stu-id="28fbb-106">**To enable Truncate on Checkpoint in Microsoft SQL Server 6.5**</span></span>

1.  <span data-ttu-id="28fbb-107">Запустите Microsoft SQL Server Enterprise Manager, откройте дерево для сервера, а затем откройте дерево устройств баз данных.</span><span class="sxs-lookup"><span data-stu-id="28fbb-107">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="28fbb-108">Дважды щелкните имя базы данных, в которой будет включена эта функция.</span><span class="sxs-lookup"><span data-stu-id="28fbb-108">Double-click the name of the database on which this feature will be enabled.</span></span>

3.  <span data-ttu-id="28fbb-109">На вкладке **база данных** выберите **усечение**.</span><span class="sxs-lookup"><span data-stu-id="28fbb-109">From the **Database** tab, select **Truncate**.</span></span>

4.  <span data-ttu-id="28fbb-110">На вкладке **Параметры** выберите пункт **усечение журнала на контрольной точке**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="28fbb-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="28fbb-111">**Включение усечения для контрольной точки в Microsoft SQL Server 7,0**</span><span class="sxs-lookup"><span data-stu-id="28fbb-111">**To enable Truncate on Checkpoint in Microsoft SQL Server 7.0**</span></span>

1.  <span data-ttu-id="28fbb-112">Запустите Microsoft SQL Server Enterprise Manager, откройте дерево для сервера, а затем откройте дерево баз данных.</span><span class="sxs-lookup"><span data-stu-id="28fbb-112">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</span></span>

2.  <span data-ttu-id="28fbb-113">Щелкните правой кнопкой мыши имя базы данных, в которой будет включена эта функция, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="28fbb-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span></span>

3.  <span data-ttu-id="28fbb-114">На вкладке **Параметры** выберите пункт **усечение журнала на контрольной точке**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="28fbb-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="28fbb-115">Для получения дополнительных сведений о функции **Truncate for Checkpoint** обратитесь к документации по Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="28fbb-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span></span>

