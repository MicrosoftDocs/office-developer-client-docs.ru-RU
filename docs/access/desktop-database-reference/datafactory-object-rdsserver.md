---
title: Объект DataFactory (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77cd06992ef0062859d0a1372d115f8e65246a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294479"
---
# <a name="datafactory-object-rdsserver"></a><span data-ttu-id="a060d-102">Объект DataFactory (RDSServer)</span><span class="sxs-lookup"><span data-stu-id="a060d-102">DataFactory object (RDSServer)</span></span>


<span data-ttu-id="a060d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a060d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a060d-104">Этот бизнес-объект на стороне сервера по умолчанию реализует методы, которые предоставляют доступ на чтение и записи к указанным источникам данных для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="a060d-104">This default server-side business object implements methods that provide read/write data access to specified data sources for client-side applications.</span></span>

## <a name="remarks"></a><span data-ttu-id="a060d-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="a060d-105">Remarks</span></span>

<span data-ttu-id="a060d-106">Объект **RDSServer.DataFactory** разработан как объект автоматизации на стороне сервера, который получает клиентские запросы.</span><span class="sxs-lookup"><span data-stu-id="a060d-106">The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests.</span></span> <span data-ttu-id="a060d-107">В реализации в Интернете он находится на веб-сервере и был созважен компонентом ADISAPI.</span><span class="sxs-lookup"><span data-stu-id="a060d-107">In an Internet implementation, it resides on a web server and is instantiated by the ADISAPI component.</span></span> <span data-ttu-id="a060d-108">Объект **RDSServer.DataFactory** предоставляет доступ на чтение и записи к указанным источникам данных, но не содержит логику проверки или бизнес-правил.</span><span class="sxs-lookup"><span data-stu-id="a060d-108">The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="a060d-109">При использовании метода, доступного как в **RDSServer.DataFactory,** так и [в RDS. Объекты DataControl,](datacontrol-object-rds.md) служба удаленных данных использует **RDS. Версия DataControl** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a060d-109">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default.</span></span> <span data-ttu-id="a060d-110">По умолчанию предполагается базовый сценарий программирования, в котором **RDSServer.DataFactory** выступает в качестве универсального бизнес-объекта на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="a060d-110">The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<span data-ttu-id="a060d-111">Чтобы веб-приложение обрабатывал обработку на стороне сервера, можно **заменить RDSServer.DataFactory** пользовательским бизнес-объектом.</span><span class="sxs-lookup"><span data-stu-id="a060d-111">If you want your web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>

<span data-ttu-id="a060d-112">Можно создать серверные бизнес-объекты, которые вызовят методы **RDSServer.DataFactory,** такие как [Query](query-method-rds.md) и [CreateRecordset.](createrecordset-method-rds.md)</span><span class="sxs-lookup"><span data-stu-id="a060d-112">You can create server-side business objects that call the **RDSServer.DataFactory** methods, such as [Query](query-method-rds.md) and [CreateRecordset](createrecordset-method-rds.md).</span></span> <span data-ttu-id="a060d-113">Это полезно, если вы хотите добавить функциональные возможности в бизнес-объекты, но воспользоваться преимуществами существующих технологий удаленной службы данных.</span><span class="sxs-lookup"><span data-stu-id="a060d-113">This is helpful if you want to add functionality to your business objects, but take advantage of existing Remote Data Service technologies.</span></span>

<span data-ttu-id="a060d-114">ИД класса для объекта **RDSServer.DataFactory** — 9381D8F5-0288-11D0-9501-00AA00B911A5.</span><span class="sxs-lookup"><span data-stu-id="a060d-114">The class ID for the **RDSServer.DataFactory** object is 9381D8F5-0288-11D0-9501-00AA00B911A5.</span></span>

