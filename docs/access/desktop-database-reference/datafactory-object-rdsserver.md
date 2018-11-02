---
title: Объект DataFactory (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4090b517dfdbe6d6870c04bf4118addad861ad95
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910637"
---
# <a name="datafactory-object-rdsserver"></a><span data-ttu-id="15cc7-102">Объект DataFactory (RDSServer)</span><span class="sxs-lookup"><span data-stu-id="15cc7-102">DataFactory object (RDSServer)</span></span>


<span data-ttu-id="15cc7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="15cc7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="15cc7-104">Этот объект по умолчанию на сервере business реализует методы, обеспечивающие доступ к данным чтение и запись к источникам данных для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="15cc7-104">This default server-side business object implements methods that provide read/write data access to specified data sources for client-side applications.</span></span>

## <a name="remarks"></a><span data-ttu-id="15cc7-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="15cc7-105">Remarks</span></span>

<span data-ttu-id="15cc7-106">Объект **RDSServer.DataFactory** разработан как объект автоматизации на сервере, которая принимает запросы клиентов.</span><span class="sxs-lookup"><span data-stu-id="15cc7-106">The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests.</span></span> <span data-ttu-id="15cc7-107">В реализацию Интернета он находится на веб-сервере и создается компонентом ADISAPI.</span><span class="sxs-lookup"><span data-stu-id="15cc7-107">In an Internet implementation, it resides on a web server and is instantiated by the ADISAPI component.</span></span> <span data-ttu-id="15cc7-108">Объект **RDSServer.DataFactory** предоставляет доступ на чтение и запись к источникам данных, но не содержит логику проверки или бизнес-правил.</span><span class="sxs-lookup"><span data-stu-id="15cc7-108">The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="15cc7-109">При использовании метода, который доступен в **RDSServer.DataFactory** и [RDS. DataControl](datacontrol-object-rds.md) объекты удаленных данных служба использует **RDS. DataControl** версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="15cc7-109">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default.</span></span> <span data-ttu-id="15cc7-110">По умолчанию предполагается базового сценария программирования, где **RDSServer.DataFactory** выступает в качестве универсального на сервере бизнес-объект.</span><span class="sxs-lookup"><span data-stu-id="15cc7-110">The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<span data-ttu-id="15cc7-111">Если необходимо, чтобы веб-приложение для обработки задач обработки на сервере, можно заменить **RDSServer.DataFactory** пользовательский бизнес-объект.</span><span class="sxs-lookup"><span data-stu-id="15cc7-111">If you want your web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>

<span data-ttu-id="15cc7-112">Можно создать бизнес-сервере объекты, которые могут вызывать **RDSServer.DataFactory** методы, такие как [CreateRecordset](createrecordset-method-rds.md)и [запросов](query-method-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="15cc7-112">You can create server-side business objects that call the **RDSServer.DataFactory** methods, such as [Query](query-method-rds.md) and [CreateRecordset](createrecordset-method-rds.md).</span></span> <span data-ttu-id="15cc7-113">Эта функция полезна, если вы хотите добавить функциональные возможности бизнес-объектов, но преимуществами существующих технологий удаленной службы данных.</span><span class="sxs-lookup"><span data-stu-id="15cc7-113">This is helpful if you want to add functionality to your business objects, but take advantage of existing Remote Data Service technologies.</span></span>

<span data-ttu-id="15cc7-114">Идентификатор класса для объекта **RDSServer.DataFactory** — 9381D8F5-0288-11 D 0-9501-00AA00B911A5.</span><span class="sxs-lookup"><span data-stu-id="15cc7-114">The class ID for the **RDSServer.DataFactory** object is 9381D8F5-0288-11D0-9501-00AA00B911A5.</span></span>

