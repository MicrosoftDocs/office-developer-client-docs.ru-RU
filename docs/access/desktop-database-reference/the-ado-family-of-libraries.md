---
title: Семейство библиотек ADO
TOCTitle: The ADO family of libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 296e05118054ec045c23cd92a399afdc3cddd9a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313974"
---
# <a name="the-ado-family-of-libraries"></a><span data-ttu-id="f6458-102">Семейство библиотек ADO</span><span class="sxs-lookup"><span data-stu-id="f6458-102">The ADO family of libraries</span></span>

<span data-ttu-id="f6458-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6458-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6458-104">Семейство ADO состоит из трех основных библиотек: ADO (включая RDS), ADO MD и ADOX.</span><span class="sxs-lookup"><span data-stu-id="f6458-104">Three major libraries make up the ADO family: ADO (including RDS), ADO MD, and ADOX.</span></span>

## <a name="ado"></a><span data-ttu-id="f6458-105">ОБЪЕКТЫ</span><span class="sxs-lookup"><span data-stu-id="f6458-105">ADO</span></span>

<span data-ttu-id="f6458-106">ADO позволяет клиентским приложениям получать данные с сервера баз данных и управлять ими с помощью поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f6458-106">ADO enables your client applications to access and manipulate data from a database server through an OLE DB provider.</span></span> <span data-ttu-id="f6458-107">Основные преимущества ADO — простота использования, высокая скорость, недостаток памяти и небольшое место на диске.</span><span class="sxs-lookup"><span data-stu-id="f6458-107">The primary benefits of ADO are ease of use, high speed, low memory overhead, and a small disk footprint.</span></span> <span data-ttu-id="f6458-108">ADO поддерживает основные функции для создания клиентских и серверных и веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="f6458-108">ADO supports key features for building client/server and web-based applications.</span></span>

<span data-ttu-id="f6458-109">Кроме того, ADO поддерживает удаленную службу данных (RDS), с помощью которой можно перемещать данные с сервера в клиентское приложение или веб-страницу, управлять данными на клиенте и возвращать обновления на сервер в едином цикле обработки.</span><span class="sxs-lookup"><span data-stu-id="f6458-109">ADO also features Remote Data Service (RDS), by which you can move data from a server to a client application or webpage, manipulate the data on the client, and return updates to the server in a single round trip.</span></span>

## <a name="ado-md"></a><span data-ttu-id="f6458-110">ADO MD</span><span class="sxs-lookup"><span data-stu-id="f6458-110">ADO MD</span></span>

<span data-ttu-id="f6458-111">Объекты данных Microsoft ActiveX (многомерные) (ADO MD) обеспечивают простой доступ к многомерным данным из таких языков, как Microsoft Visual Basic, Microsoft Visual C++ и Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="f6458-111">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++.</span></span> <span data-ttu-id="f6458-112">ADO MD расширяет ADO, чтобы включить объекты, относящиеся к многомерным данным, например объектам **CubeDef** и набору **ячеек** .</span><span class="sxs-lookup"><span data-stu-id="f6458-112">ADO MD extends ADO to include objects specific to multidimensional data, such as the **CubeDef** and **Cellset** objects.</span></span> <span data-ttu-id="f6458-113">С помощью ADO MD можно просматривать многомерную схему, запрашивать куб и получать результаты.</span><span class="sxs-lookup"><span data-stu-id="f6458-113">With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="f6458-114">Как и в ADO, ADO MD использует поставщика OLE DB для получения доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="f6458-114">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data.</span></span> <span data-ttu-id="f6458-115">Для работы с ADO MD поставщик должен быть многомерным поставщиком данных (МДП), как определено в спецификации OLE DB для OLAP.</span><span class="sxs-lookup"><span data-stu-id="f6458-115">To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification.</span></span> <span data-ttu-id="f6458-116">Мдпс представляют данные в многомерных представлениях, а не в табличных поставщиках данных (Тдпс), которые представляют данные в табличных представлениях.</span><span class="sxs-lookup"><span data-stu-id="f6458-116">MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views.</span></span> <span data-ttu-id="f6458-117">Для получения более подробных сведений о синтаксисе и возМожностях, поддерживаемых поставщиком, обратитесь к документации по поставщику OLE DB для поставщика OLAP.</span><span class="sxs-lookup"><span data-stu-id="f6458-117">Refer to the documentation for your OLE DB for OLAP provider for more detailed information about the specific syntax and behaviors supported by your provider.</span></span>

## <a name="adox"></a><span data-ttu-id="f6458-118">ADOX</span><span class="sxs-lookup"><span data-stu-id="f6458-118">ADOX</span></span>

<span data-ttu-id="f6458-119">Расширения объектов данных Microsoft ActiveX для языка определения данных и безопасности (ADOX) являются расширением объектов ADO и программной модели.</span><span class="sxs-lookup"><span data-stu-id="f6458-119">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model.</span></span> <span data-ttu-id="f6458-120">ADOX включает объекты для создания и изменения схемы, а также для обеспечения безопасности.</span><span class="sxs-lookup"><span data-stu-id="f6458-120">ADOX includes objects for schema creation and modification as well as security.</span></span> <span data-ttu-id="f6458-121">Так как это подход, основанный на объектах, для управления схемой, вы можете написать код, который будет работать с разными источниками данных независимо от различий в их исходных синтаксисах.</span><span class="sxs-lookup"><span data-stu-id="f6458-121">Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="f6458-122">ADOX — вспомогательная библиотека для базовых объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="f6458-122">ADOX is a companion library to the core ADO objects.</span></span> <span data-ttu-id="f6458-123">Он предоставляет доступ к дополнительным объектам для создания, изменения и удаления объектов схемы, таких как таблицы и процедуры.</span><span class="sxs-lookup"><span data-stu-id="f6458-123">It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures.</span></span> <span data-ttu-id="f6458-124">Он также включает объекты безопасности для поддержки пользователей и групп, а также для предоставления и отзыва разрешений на объекты.</span><span class="sxs-lookup"><span data-stu-id="f6458-124">It also includes security objects to maintain users and groups, and to grant and revoke permissions on objects.</span></span>

