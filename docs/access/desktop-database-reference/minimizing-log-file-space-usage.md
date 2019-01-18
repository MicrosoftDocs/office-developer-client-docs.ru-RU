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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715279"
---
# <a name="minimizing-log-file-space-usage"></a><span data-ttu-id="46eba-102">Минимизация места, занимаемого файлом журнала</span><span class="sxs-lookup"><span data-stu-id="46eba-102">Minimizing log file space usage</span></span>

<span data-ttu-id="46eba-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46eba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46eba-104">Файл журнала можно указать быстро (таким образом, остановка работы сервера) при наличии больших объемов активности в базе данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="46eba-104">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database.</span></span> <span data-ttu-id="46eba-105">Файл журнала можно включить **Truncate на контрольной точки** для значительного увеличения работы файла журнала для базы данных.</span><span class="sxs-lookup"><span data-stu-id="46eba-105">You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span></span>

<span data-ttu-id="46eba-106">**Чтобы включить Truncate на контрольной точки в Microsoft SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="46eba-106">**To enable Truncate on Checkpoint in Microsoft SQL Server 6.5**</span></span>

1.  <span data-ttu-id="46eba-107">Запустите Microsoft SQL Server Enterprise Manager, откройте дерево для сервера и откройте дерево устройств базы данных.</span><span class="sxs-lookup"><span data-stu-id="46eba-107">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="46eba-108">Дважды щелкните имя базы данных, на котором эта возможность включена.</span><span class="sxs-lookup"><span data-stu-id="46eba-108">Double-click the name of the database on which this feature will be enabled.</span></span>

3.  <span data-ttu-id="46eba-109">Вкладка " **базы данных** " выберите **Truncate**.</span><span class="sxs-lookup"><span data-stu-id="46eba-109">From the **Database** tab, select **Truncate**.</span></span>

4.  <span data-ttu-id="46eba-110">На вкладке **Параметры** выберите **Усечение журнала на контрольной точки**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="46eba-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="46eba-111">**Чтобы включить Truncate на контрольной точки в Microsoft SQL Server 7.0**</span><span class="sxs-lookup"><span data-stu-id="46eba-111">**To enable Truncate on Checkpoint in Microsoft SQL Server 7.0**</span></span>

1.  <span data-ttu-id="46eba-112">Запустите Microsoft SQL Server Enterprise Manager, откройте дерево для сервера и откройте дерево базы данных.</span><span class="sxs-lookup"><span data-stu-id="46eba-112">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</span></span>

2.  <span data-ttu-id="46eba-113">Щелкните правой кнопкой мыши имя базы данных, на котором этот компонент будет установлен и выберите команду **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="46eba-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span></span>

3.  <span data-ttu-id="46eba-114">На вкладке **Параметры** выберите **Усечение журнала на контрольной точки**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="46eba-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="46eba-115">Дополнительные сведения о функции **Truncate на контрольной точки** документации Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="46eba-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span></span>

