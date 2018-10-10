---
title: The ADO Family of Libraries
TOCTitle: The ADO Family of Libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9de96854eb08ff73fe9f70edf35dee972fd1a31e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480434"
---
# <a name="the-ado-family-of-libraries"></a><span data-ttu-id="c8f81-102">The ADO Family of Libraries</span><span class="sxs-lookup"><span data-stu-id="c8f81-102">The ADO Family of Libraries</span></span>


<span data-ttu-id="c8f81-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8f81-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="c8f81-104">Три основных библиотек составляют семейство ADO: ADO (в том числе служб удаленных рабочих СТОЛОВ), ADO MD и ADOX.</span><span class="sxs-lookup"><span data-stu-id="c8f81-104">Three major libraries make up the ADO family: ADO (including RDS), ADO MD, and ADOX.</span></span>

## <a name="ado"></a><span data-ttu-id="c8f81-105">ADO</span><span class="sxs-lookup"><span data-stu-id="c8f81-105">ADO</span></span>

<span data-ttu-id="c8f81-106">ADO позволяет клиентских приложениях для доступа и работы с данными на сервере базы данных через поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c8f81-106">ADO enables your client applications to access and manipulate data from a database server through an OLE DB provider.</span></span> <span data-ttu-id="c8f81-107">Основными преимуществами ADO, простота использования, высокой скорости, нагрузка на нехватки памяти и объем небольшой диска.</span><span class="sxs-lookup"><span data-stu-id="c8f81-107">The primary benefits of ADO are ease of use, high speed, low memory overhead, and a small disk footprint.</span></span> <span data-ttu-id="c8f81-108">ADO поддерживает основные функции для построения клиента и сервера и веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c8f81-108">ADO supports key features for building client/server and Web-based applications.</span></span>

<span data-ttu-id="c8f81-109">ADO также функций приложения-службы удаленных данных (RDS), с помощью которого можно перемещение данных с сервера в клиентском приложении или веб-страницу, работы с данными на стороне клиента и возврата обновлений на сервер в одном кругового пути.</span><span class="sxs-lookup"><span data-stu-id="c8f81-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or Web page, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="c8f81-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="c8f81-110">ADO MD</span></span>

<span data-ttu-id="c8f81-111">Microsoft ActiveX Data Objects (ADO MD) (многомерные) обеспечивает быстрый доступ к многомерным данным из языков, такие как Microsoft Visual Basic, Microsoft Visual C++ и Microsoft Visual J ++.</span><span class="sxs-lookup"><span data-stu-id="c8f81-111">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++.</span></span> <span data-ttu-id="c8f81-112">ADO MD расширяет ADO для включения объектов, относящихся к многомерных данных, таких как объекты **CubeDef** и **ячеек** .</span><span class="sxs-lookup"><span data-stu-id="c8f81-112">ADO MD extends ADO to include objects specific to multidimensional data, such as the **CubeDef** and **Cellset** objects.</span></span> <span data-ttu-id="c8f81-113">С помощью ADO MD можно выбрать многомерные схему, запроса куба и получения результатов.</span><span class="sxs-lookup"><span data-stu-id="c8f81-113">With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="c8f81-114">Как и ADO ADO MD использует поставщика OLE DB для получения доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="c8f81-114">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data.</span></span> <span data-ttu-id="c8f81-115">Для работы с ADO MD, поставщик должен быть многомерные данные поставщика (MDP), определенный спецификации OLE DB для OLAP.</span><span class="sxs-lookup"><span data-stu-id="c8f81-115">To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification.</span></span> <span data-ttu-id="c8f81-116">MDPs представления данных в отличие от поставщиков табличных данных (за) многомерные представлениях, представляющих данные в табличных представлений.</span><span class="sxs-lookup"><span data-stu-id="c8f81-116">MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views.</span></span> <span data-ttu-id="c8f81-117">Обратитесь к документации для вашей OLE DB для OLAP поставщика более подробные сведения о конкретных синтаксис и поведение, поддерживаемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="c8f81-117">Refer to the documentation for your OLE DB for OLAP provider for more detailed information about the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="c8f81-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="c8f81-118">ADOX</span></span>

<span data-ttu-id="c8f81-119">Расширения объектов данных Microsoft ActiveX для языка определения данных и безопасности (ADOX) — это расширение объекты ADO и модели программирования.</span><span class="sxs-lookup"><span data-stu-id="c8f81-119">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model.</span></span> <span data-ttu-id="c8f81-120">ADOX включает в себя объекты для создания схемы и изменения, а также безопасности.</span><span class="sxs-lookup"><span data-stu-id="c8f81-120">ADOX includes objects for schema creation and modification as well as security.</span></span> <span data-ttu-id="c8f81-121">Так как они объектно ориентированный подход к схеме выполнение различных операций, можно написать код, будут работать в различных данных источников независимо от того, различия в свой собственный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="c8f81-121">Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="c8f81-122">ADOX — это companion Библиотека базовых объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="c8f81-122">ADOX is a companion library to the core ADO objects.</span></span> <span data-ttu-id="c8f81-123">Она предоставляет дополнительные объекты для создания, изменения и удаления объектов схемы, например таблицы и процедуры.</span><span class="sxs-lookup"><span data-stu-id="c8f81-123">It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures.</span></span> <span data-ttu-id="c8f81-124">Он также включает объекты безопасности обслуживание пользователей и групп, а также предоставления и отмены разрешений для объектов.</span><span class="sxs-lookup"><span data-stu-id="c8f81-124">It also includes security objects to maintain users and groups, and to grant and revoke permissions on objects.</span></span>

