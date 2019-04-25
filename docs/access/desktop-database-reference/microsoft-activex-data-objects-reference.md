---
title: Справочник по объектам данных Microsoft ActiveX
TOCTitle: Microsoft ActiveX Data Objects Reference
ms:assetid: 235fc575-8a2e-913c-fa3d-bb86256733f9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249010(v=office.15)
ms:contentKeyID: 48543728
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c1fee657c0d6ecd319157f704df2b1c5a900be3b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289121"
---
# <a name="microsoft-activex-data-objects-reference"></a><span data-ttu-id="7d7bc-102">Справочник по объектам данных Microsoft ActiveX</span><span class="sxs-lookup"><span data-stu-id="7d7bc-102">Microsoft ActiveX Data Objects reference</span></span>

<span data-ttu-id="7d7bc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d7bc-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="purpose"></a><span data-ttu-id="7d7bc-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="7d7bc-104">Purpose</span></span>

<span data-ttu-id="7d7bc-105">Объекты данных ActiveX (ADO) позволяют клиентским приложениям получать доступ к данным из сервера базы данных и управлять ими с помощью поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-105">Microsoft ActiveX Data Objects (ADO) enable your client applications to access and manipulate data from a database server through an OLE DB provider.</span></span> <span data-ttu-id="7d7bc-106">Их основными преимуществами являются простота использования, высокая скорость, малое использование ресурсов памяти и небольшой занимаемый размер диска.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-106">Its primary benefits are ease of use, high speed, low memory overhead, and a small disk footprint.</span></span> <span data-ttu-id="7d7bc-107">ADO поддерживают основные функции создания клиентских, серверных и веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-107">ADO supports key features for building client/server and web-based applications.</span></span>

## <a name="rds"></a><span data-ttu-id="7d7bc-108">RDS</span><span class="sxs-lookup"><span data-stu-id="7d7bc-108">RDS methods</span></span>

<span data-ttu-id="7d7bc-109">ADO также используют службу удаленных данных (RDS), с помощью которой можно перемещать данные с сервера на клиентское приложение или веб-страницу, работать с данными в клиенте и возвращать обновления на сервер за один круговой путь.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or webpage, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="7d7bc-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="7d7bc-110">ADO MD collections</span></span>

<span data-ttu-id="7d7bc-111">Объекты данных Microsoft ActiveX (многомерные) (ADO MD) обеспечивают простой доступ к многомерным данным из таких языков, как Microsoft Visual Basic, Microsoft Visual C++ и Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-111">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++.</span></span> <span data-ttu-id="7d7bc-112">ADO MD расширяют объекты данных Microsoft ActiveX (ADO) для включения объектов, связанных с многомерными данными, например CubeDef и Cellset.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-112">ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the CubeDef and Cellset objects.</span></span> <span data-ttu-id="7d7bc-113">С помощью ADO MD можно просматривать многомерные схемы, запрашивать кубы и получать результаты.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-113">With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="7d7bc-114">Как и ADO, ADO MD используют основного поставщика OLE DB для получения доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-114">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data.</span></span> <span data-ttu-id="7d7bc-115">Для работы с ADO MD должен использоваться поставщик многомерных данных (MDP), как определено в OLE DB для спецификации OLAP.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-115">To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification.</span></span> <span data-ttu-id="7d7bc-116">Поставщики MDP отображают данные в многомерных представлениях в отличие от поставщиков табличных данных (TDP), отображающих данные в табличных представлениях.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-116">MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views.</span></span> <span data-ttu-id="7d7bc-117">Дополнительные сведения о конкретном синтаксисе и поддерживаемых поставщиком действиях см. в документации для своего поставщика OLAP OLE DB.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-117">Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="7d7bc-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="7d7bc-118">ADOX properties</span></span>

<span data-ttu-id="7d7bc-119">Расширения объектов данных Microsoft ActiveX для языка описания данных и безопасности (ADOX) — это расширение для объектов и модели программирования ADO.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-119">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model.</span></span> <span data-ttu-id="7d7bc-120">ADOX включают объекты для создания и изменения схемы, а также для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-120">ADOX includes objects for schema creation and modification, as well as security.</span></span> <span data-ttu-id="7d7bc-121">Так как это основанный на объектах способ управления схемой, можно написать код, который будет работать с разными источниками данных, независимо от различий в их собственных синтаксисах.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-121">Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="7d7bc-122">ADOX — это дополнительная библиотека для основных объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-122">ADOX is a companion library to the core ADO objects.</span></span> <span data-ttu-id="7d7bc-123">В ней представлены дополнительные объекты для создания, изменения и удаления объектов схемы, таких как таблицы и процедуры.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-123">It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures.</span></span> <span data-ttu-id="7d7bc-124">В ней также содержатся объекты безопасности для обслуживания пользователей и групп, а также предоставления и отзыва разрешений для объектов.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-124">It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

## <a name="ado-25-main-components"></a><span data-ttu-id="7d7bc-125">Основные компоненты ADO 2.5</span><span class="sxs-lookup"><span data-stu-id="7d7bc-125">ADO 2.5 main components</span></span>

- <span data-ttu-id="7d7bc-126">[Руководство для программиста](ado-programmer-s-guide.md): введение в использование ADO, RDS, ADO MD и ADOX.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-126">[Programmer's guide](ado-programmer-s-guide.md): An introduction to using ADO, RDS, ADO MD, and ADOX.</span></span>

- <span data-ttu-id="7d7bc-127">[Справочник программиста](ado-programmer-s-reference-topics.md): в этом разделе документации по ADO содержатся статьи для каждого объекта, коллекции, свойства, динамического свойства, метода, события и перечисления ADO, RDS, ADO MD и ADOX.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-127">[Programmer's reference](ado-programmer-s-reference-topics.md): This section of the ADO documentation contains topics for each ADO, RDS, ADO MD, and ADOX object, collection, property, dynamic property, method, event, and enumeration.</span></span>

## <a name="feedback"></a><span data-ttu-id="7d7bc-128">Обратная связь</span><span class="sxs-lookup"><span data-stu-id="7d7bc-128">Feedback</span></span>

<span data-ttu-id="7d7bc-129">Вы можете отправить отзыв о документации по ADO или примерах непосредственно группе разработчиков документации по ADO.</span><span class="sxs-lookup"><span data-stu-id="7d7bc-129">You can send feedback about ADO documentation or samples directly to the ADO documentation team.</span></span>

