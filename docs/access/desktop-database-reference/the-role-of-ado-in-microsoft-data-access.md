---
title: The Role of ADO in Microsoft Data Access
TOCTitle: The Role of ADO in Microsoft Data Access
ms:assetid: e9087ec8-850b-ebbe-369a-a5987a528de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250180(v=office.15)
ms:contentKeyID: 48548433
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 91f591513e0a35a70d157b0a640c87efc961fe22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314037"
---
# <a name="role-of-ado-in-microsoft-data-access"></a><span data-ttu-id="0a6db-102">Роль ADO в Microsoft Data Access</span><span class="sxs-lookup"><span data-stu-id="0a6db-102">Role of ADO in Microsoft Data Access</span></span>

<span data-ttu-id="0a6db-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a6db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0a6db-104">Компоненты доступа к данным MDAC предоставляют доступ к данным независимо от хранилищ, средств и языков.</span><span class="sxs-lookup"><span data-stu-id="0a6db-104">The Microsoft Data Access Components (MDAC) provide data access that is independent of data stores, tools, and languages.</span></span> <span data-ttu-id="0a6db-105">Он предоставляет высокоуровневый, простой в использовании интерфейс и высокоуровневый высокопроизводительный интерфейс для практически любого доступного хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="0a6db-105">It provides a high-level, easy-to-use interface, and a low-level, high-performance interface to practically any data store available.</span></span> <span data-ttu-id="0a6db-106">Эту гибкость можно использовать для интеграции различных хранилищ данных и выбора средств, приложений и служб платформы для создания правильных решений.</span><span class="sxs-lookup"><span data-stu-id="0a6db-106">You can use this flexibility to integrate diverse data stores and use your choice of tools, applications, and platform services to create the right solutions for your needs.</span></span> <span data-ttu-id="0a6db-107">Эти технологии предоставляют базовую среду для общего доступа к данным в операционных системах Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0a6db-107">These technologies provide the basic framework for general-purpose data access in Microsoft Windows operating systems.</span></span>

<span data-ttu-id="0a6db-108">В MDAC существует три основных технологии.</span><span class="sxs-lookup"><span data-stu-id="0a6db-108">There are three primary technologies in MDAC.</span></span> <span data-ttu-id="0a6db-109">Объекты данных ActiveX (ADO) — это высокоуровневый, простой в использовании интерфейс для OLE DB.</span><span class="sxs-lookup"><span data-stu-id="0a6db-109">ActiveX Data Objects (ADO) is a high-level, easy-to-use interface to OLE DB.</span></span> <span data-ttu-id="0a6db-110">OLE DB — это высокоуровневая высокопроизводительный интерфейс для различных хранилищ данных.</span><span class="sxs-lookup"><span data-stu-id="0a6db-110">OLE DB is a low-level, high-performance interface to a variety of data stores.</span></span> <span data-ttu-id="0a6db-111">ADO и OLE DB могут работать с реляционными (табличными) и нереляционными (иерархическими и потоками) данными.</span><span class="sxs-lookup"><span data-stu-id="0a6db-111">ADO and OLE DB both can work with relational (tabular) and nonrelational (hierarchical or stream) data.</span></span> <span data-ttu-id="0a6db-112">Наконец, открытое подключение к базам данных (ODBC) — это другой высокопроизводительный интерфейс, предназначенный специально для хранилищ реляционных данных.</span><span class="sxs-lookup"><span data-stu-id="0a6db-112">Finally, Open Database Connectivity (ODBC) is another low-level, high-performance interface that is designed specifically for relational data stores.</span></span>

<span data-ttu-id="0a6db-113">ADO предоставляет уровень абстракции между клиентским приложением или приложением среднего уровня и интерфейсами низкоуровневых баз данных OLE DB.</span><span class="sxs-lookup"><span data-stu-id="0a6db-113">ADO provides a layer of abstraction between your client or middle-tier application and the low-level OLE DB interfaces.</span></span> <span data-ttu-id="0a6db-114">ADO использует небольшой набор объектов автоматизации для создания простого и эффективного интерфейса OLE DB.</span><span class="sxs-lookup"><span data-stu-id="0a6db-114">ADO uses a small set of Automation objects to provide a simple and efficient interface to OLE DB.</span></span> <span data-ttu-id="0a6db-115">Этот интерфейс делает ADO идеальным выбором для разработчиков на более высоких языках, таких как Visual Basic и даже VBScript, которые хотят получить доступ к данным без необходимости изучать структуры COM и OLE DB.</span><span class="sxs-lookup"><span data-stu-id="0a6db-115">This interface makes ADO the perfect choice for developers in higher level languages, such as Visual Basic and even VBScript, who want to access data without having to learn the intricacies of COM and OLE DB.</span></span>

