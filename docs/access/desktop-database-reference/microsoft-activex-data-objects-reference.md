---
title: Справочник по Microsoft ActiveX Data Objects
TOCTitle: Microsoft ActiveX Data Objects Reference
ms:assetid: 235fc575-8a2e-913c-fa3d-bb86256733f9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249010(v=office.15)
ms:contentKeyID: 48543728
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5426dd17e174c0aa95517885fd43e7d00f21342b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481474"
---
# <a name="microsoft-activex-data-objects-reference"></a><span data-ttu-id="9a853-102">Справочник по Microsoft ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="9a853-102">Microsoft ActiveX Data Objects reference</span></span>

<span data-ttu-id="9a853-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a853-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="purpose"></a><span data-ttu-id="9a853-104">Цель</span><span class="sxs-lookup"><span data-stu-id="9a853-104">Purpose</span></span>

<span data-ttu-id="9a853-105">Microsoft ActiveX Data Objects (ADO) Включение клиентских приложениях для доступа и работы с данными на сервере базы данных через поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="9a853-105">Microsoft ActiveX Data Objects (ADO) enable your client applications to access and manipulate data from a database server through an OLE DB provider.</span></span> <span data-ttu-id="9a853-106">Его основных преимуществ, простота использования, высокой скорости, нагрузка на нехватки памяти и объем небольшой диска.</span><span class="sxs-lookup"><span data-stu-id="9a853-106">Its primary benefits are ease of use, high speed, low memory overhead, and a small disk footprint.</span></span> <span data-ttu-id="9a853-107">ADO поддерживает основные функции для построения клиента и сервера и веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="9a853-107">ADO supports key features for building client/server and Web-based applications.</span></span>

## <a name="rds"></a><span data-ttu-id="9a853-108">СЛУЖБ УДАЛЕННЫХ РАБОЧИХ СТОЛОВ</span><span class="sxs-lookup"><span data-stu-id="9a853-108">RDS</span></span>

<span data-ttu-id="9a853-109">ADO также функций приложения-службы удаленных данных (RDS), с помощью которого можно перемещение данных с сервера в клиентском приложении или веб-страницу, работы с данными на стороне клиента и возврата обновлений на сервер в одном кругового пути.</span><span class="sxs-lookup"><span data-stu-id="9a853-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or Web page, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="9a853-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="9a853-110">ADO MD</span></span>

<span data-ttu-id="9a853-111">Microsoft ActiveX Data Objects (ADO MD) (многомерные) обеспечивает быстрый доступ к многомерным данным из языков, такие как Microsoft Visual Basic, Microsoft Visual C++ и Microsoft Visual J ++.</span><span class="sxs-lookup"><span data-stu-id="9a853-111">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++.</span></span> <span data-ttu-id="9a853-112">ADO MD расширяет возможности Microsoft ActiveX Data Objects (ADO) для включения объектов, относящихся к многомерных данных, таких как объекты CubeDef и ячеек.</span><span class="sxs-lookup"><span data-stu-id="9a853-112">ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the CubeDef and Cellset objects.</span></span> <span data-ttu-id="9a853-113">С помощью ADO MD можно выбрать многомерные схему, запроса куба и получения результатов.</span><span class="sxs-lookup"><span data-stu-id="9a853-113">With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="9a853-114">Как и ADO ADO MD использует поставщика OLE DB для получения доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="9a853-114">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data.</span></span> <span data-ttu-id="9a853-115">Для работы с ADO MD, поставщик должен быть многомерные данные поставщика (MDP), определенный спецификации OLE DB для OLAP.</span><span class="sxs-lookup"><span data-stu-id="9a853-115">To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification.</span></span> <span data-ttu-id="9a853-116">MDPs представления данных в отличие от поставщиков табличных данных (за) многомерные представлениях, представляющих данные в табличных представлений.</span><span class="sxs-lookup"><span data-stu-id="9a853-116">MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views.</span></span> <span data-ttu-id="9a853-117">Обратитесь к документации для поставщика OLE DB для OLAP более подробные сведения о конкретных синтаксис и поведение поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="9a853-117">Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="9a853-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="9a853-118">ADOX</span></span>

<span data-ttu-id="9a853-119">Расширения объектов данных Microsoft ActiveX для языка определения данных и безопасности (ADOX) — это расширение объекты ADO и модели программирования.</span><span class="sxs-lookup"><span data-stu-id="9a853-119">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model.</span></span> <span data-ttu-id="9a853-120">ADOX включает в себя объекты для создания схемы и изменения, а также безопасности.</span><span class="sxs-lookup"><span data-stu-id="9a853-120">ADOX includes objects for schema creation and modification, as well as security.</span></span> <span data-ttu-id="9a853-121">Так как они объектно ориентированный подход к схеме выполнение различных операций, можно написать код, будут работать в различных данных источников независимо от того, различия в свой собственный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="9a853-121">Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="9a853-122">ADOX — это companion Библиотека базовых объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="9a853-122">ADOX is a companion library to the core ADO objects.</span></span> <span data-ttu-id="9a853-123">Она предоставляет дополнительные объекты для создания, изменения и удаления объектов схемы, например таблицы и процедуры.</span><span class="sxs-lookup"><span data-stu-id="9a853-123">It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures.</span></span> <span data-ttu-id="9a853-124">Он также включает объекты безопасности на обслуживание пользователей и групп, а также для предоставления и отмены разрешений для объектов.</span><span class="sxs-lookup"><span data-stu-id="9a853-124">It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

## <a name="ado-25-main-components"></a><span data-ttu-id="9a853-125">ADO 2.5 основных компонентов</span><span class="sxs-lookup"><span data-stu-id="9a853-125">ADO 2.5 main components</span></span>

- <span data-ttu-id="9a853-126">[Руководство программиста](ado-programmer-s-guide.md): введение в использование ADO, RDS, ADO MD и ADOX.</span><span class="sxs-lookup"><span data-stu-id="9a853-126">[Programmer's guide](ado-programmer-s-guide.md): An introduction to using ADO, RDS, ADO MD, and ADOX.</span></span>

- <span data-ttu-id="9a853-127">[Справочник программиста по](ado-programmer-s-reference-topics.md): в этом разделе документации по ADO разделы для каждого ADO, RDS, ADO MD и ADOX объект коллекции, свойства, динамические свойства, метод, события и перечисления.</span><span class="sxs-lookup"><span data-stu-id="9a853-127">[Programmer's reference](ado-programmer-s-reference-topics.md): This section of the ADO documentation contains topics for each ADO, RDS, ADO MD, and ADOX object, collection, property, dynamic property, method, event, and enumeration.</span></span>

## <a name="feedback"></a><span data-ttu-id="9a853-128">Отзывы</span><span class="sxs-lookup"><span data-stu-id="9a853-128">Feedback</span></span>

<span data-ttu-id="9a853-129">Можно отправить отзыв о документации по ADO или примеры непосредственно на группы разработчиков документации ADO.</span><span class="sxs-lookup"><span data-stu-id="9a853-129">You can send feedback about ADO documentation or samples directly to the ADO documentation team.</span></span>

