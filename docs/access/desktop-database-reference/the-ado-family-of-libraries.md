---
title: Семейство ADO библиотек
TOCTitle: The ADO family of libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 296e05118054ec045c23cd92a399afdc3cddd9a1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718219"
---
# <a name="the-ado-family-of-libraries"></a><span data-ttu-id="a4806-102">Семейство ADO библиотек</span><span class="sxs-lookup"><span data-stu-id="a4806-102">The ADO family of libraries</span></span>

<span data-ttu-id="a4806-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4806-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a4806-104">Три основных библиотек составляют семейство ADO: ADO (в том числе служб удаленных рабочих СТОЛОВ), ADO MD и ADOX.</span><span class="sxs-lookup"><span data-stu-id="a4806-104">Three major libraries make up the ADO family: ADO (including RDS), ADO MD, and ADOX.</span></span>

## <a name="ado"></a><span data-ttu-id="a4806-105">ADO</span><span class="sxs-lookup"><span data-stu-id="a4806-105">ADO</span></span>

<span data-ttu-id="a4806-106">ADO позволяет клиентских приложениях для доступа и работы с данными на сервере базы данных через поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a4806-106">ADO enables your client applications to access and manipulate data from a database server through an OLE DB provider.</span></span> <span data-ttu-id="a4806-107">Основными преимуществами ADO, простота использования, высокой скорости, нагрузка на нехватки памяти и объем небольшой диска.</span><span class="sxs-lookup"><span data-stu-id="a4806-107">The primary benefits of ADO are ease of use, high speed, low memory overhead, and a small disk footprint.</span></span> <span data-ttu-id="a4806-108">ADO поддерживает основные функции для построения клиента и сервера и веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="a4806-108">ADO supports key features for building client/server and web-based applications.</span></span>

<span data-ttu-id="a4806-109">ADO также компонентов удаленных данных службы (RDS), с помощью которого можно переместить данные из сервера в клиентском приложении или веб-страницы, работы с данными на стороне клиента и возврата обновлений на сервер в одном обращение.</span><span class="sxs-lookup"><span data-stu-id="a4806-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or webpage, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="a4806-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="a4806-110">ADO MD</span></span>

<span data-ttu-id="a4806-111">Microsoft ActiveX Data Objects (ADO MD) (многомерные) обеспечивает быстрый доступ к многомерным данным из языков, такие как Microsoft Visual Basic, Microsoft Visual C++ и Microsoft Visual J ++.</span><span class="sxs-lookup"><span data-stu-id="a4806-111">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++.</span></span> <span data-ttu-id="a4806-112">ADO MD расширяет ADO для включения объектов, относящихся к многомерных данных, таких как объекты **CubeDef** и **ячеек** .</span><span class="sxs-lookup"><span data-stu-id="a4806-112">ADO MD extends ADO to include objects specific to multidimensional data, such as the **CubeDef** and **Cellset** objects.</span></span> <span data-ttu-id="a4806-113">С помощью ADO MD можно выбрать многомерные схему, запроса куба и получения результатов.</span><span class="sxs-lookup"><span data-stu-id="a4806-113">With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="a4806-114">Как и ADO ADO MD использует поставщика OLE DB для получения доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="a4806-114">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data.</span></span> <span data-ttu-id="a4806-115">Для работы с ADO MD, поставщик должен быть многомерные данные поставщика (MDP), определенный спецификации OLE DB для OLAP.</span><span class="sxs-lookup"><span data-stu-id="a4806-115">To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification.</span></span> <span data-ttu-id="a4806-116">MDPs представления данных в отличие от поставщиков табличных данных (за) многомерные представлениях, представляющих данные в табличных представлений.</span><span class="sxs-lookup"><span data-stu-id="a4806-116">MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views.</span></span> <span data-ttu-id="a4806-117">Обратитесь к документации для вашей OLE DB для OLAP поставщика более подробные сведения о конкретных синтаксис и поведение, поддерживаемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="a4806-117">Refer to the documentation for your OLE DB for OLAP provider for more detailed information about the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="a4806-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="a4806-118">ADOX</span></span>

<span data-ttu-id="a4806-119">Расширения объектов данных Microsoft ActiveX для языка определения данных и безопасности (ADOX) — это расширение объекты ADO и модели программирования.</span><span class="sxs-lookup"><span data-stu-id="a4806-119">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model.</span></span> <span data-ttu-id="a4806-120">ADOX включает в себя объекты для создания схемы и изменения, а также безопасности.</span><span class="sxs-lookup"><span data-stu-id="a4806-120">ADOX includes objects for schema creation and modification as well as security.</span></span> <span data-ttu-id="a4806-121">Так как они объектно ориентированный подход к схеме выполнение различных операций, можно написать код, будут работать в различных данных источников независимо от того, различия в свой собственный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="a4806-121">Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="a4806-122">ADOX — это companion Библиотека базовых объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="a4806-122">ADOX is a companion library to the core ADO objects.</span></span> <span data-ttu-id="a4806-123">Она предоставляет дополнительные объекты для создания, изменения и удаления объектов схемы, например таблицы и процедуры.</span><span class="sxs-lookup"><span data-stu-id="a4806-123">It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures.</span></span> <span data-ttu-id="a4806-124">Он также включает объекты безопасности обслуживание пользователей и групп, а также предоставления и отмены разрешений для объектов.</span><span class="sxs-lookup"><span data-stu-id="a4806-124">It also includes security objects to maintain users and groups, and to grant and revoke permissions on objects.</span></span>

