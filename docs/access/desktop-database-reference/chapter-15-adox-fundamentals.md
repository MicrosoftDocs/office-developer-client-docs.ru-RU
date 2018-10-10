---
title: 'Chapter 15: ADOX Fundamentals'
TOCTitle: 'Chapter 15: ADOX Fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3869f23b93df78fd207812a85f91dd3272bd255f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482828"
---
# <a name="chapter-15-adox-fundamentals"></a><span data-ttu-id="ec25f-102">Chapter 15: ADOX Fundamentals</span><span class="sxs-lookup"><span data-stu-id="ec25f-102">Chapter 15: ADOX Fundamentals</span></span>


<span data-ttu-id="ec25f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec25f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ec25f-104">Microsoft® ActiveX® данных объекты расширения для языка определения данных и безопасности (ADOX) — это расширение объекты ADO и модели программирования.</span><span class="sxs-lookup"><span data-stu-id="ec25f-104">Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model.</span></span> <span data-ttu-id="ec25f-105">ADOX включает в себя объекты для создания схемы и изменения, а также безопасности.</span><span class="sxs-lookup"><span data-stu-id="ec25f-105">ADOX includes objects for schema creation and modification, as well as security.</span></span> <span data-ttu-id="ec25f-106">Так как они объектно ориентированный подход к схеме выполнение различных операций, можно написать код, будут работать в различных данных источников независимо от того, различия в свой собственный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="ec25f-106">Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="ec25f-107">ADOX — это companion Библиотека базовых объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="ec25f-107">ADOX is a companion library to the core ADO objects.</span></span> <span data-ttu-id="ec25f-108">Она предоставляет дополнительные объекты для создания, изменения и удаления объектов схемы, например таблицы и процедуры.</span><span class="sxs-lookup"><span data-stu-id="ec25f-108">It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures.</span></span> <span data-ttu-id="ec25f-109">Он также включает объекты безопасности на обслуживание пользователей и групп, а также для предоставления и отмены разрешений для объектов.</span><span class="sxs-lookup"><span data-stu-id="ec25f-109">It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

<span data-ttu-id="ec25f-110">Чтобы использовать ADOX со средством разработки, следует устанавливать ссылки на библиотеку типа ADOX.</span><span class="sxs-lookup"><span data-stu-id="ec25f-110">To use ADOX with your development tool, you should establish a reference to the ADOX type library.</span></span> <span data-ttu-id="ec25f-111">Описание библиотеки ADOX — это «Microsoft ADO внешний DDL и системы безопасности».</span><span class="sxs-lookup"><span data-stu-id="ec25f-111">The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security."</span></span> <span data-ttu-id="ec25f-112">Имя файла библиотеки ADOX — Msadox.dll, а идентификатор программы (ProgID) — «ADOX».</span><span class="sxs-lookup"><span data-stu-id="ec25f-112">The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX".</span></span> <span data-ttu-id="ec25f-113">Дополнительные сведения о создании ссылки на библиотеки обратитесь к документации вашего средство разработки.</span><span class="sxs-lookup"><span data-stu-id="ec25f-113">For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="ec25f-114">Поставщик Microsoft OLE DB для базы данных Microsoft Jet полностью поддерживает ADOX.</span><span class="sxs-lookup"><span data-stu-id="ec25f-114">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX.</span></span> <span data-ttu-id="ec25f-115">Некоторые возможности ADOX может не поддерживаться, в зависимости от поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="ec25f-115">Certain features of ADOX may not be supported, depending on your data provider.</span></span> <span data-ttu-id="ec25f-116">Дополнительные сведения о поддерживаемых функций с помощью поставщик Microsoft OLE DB для ODBC, поставщик Microsoft OLE DB для Oracle или Microsoft SQL Server поставщик OLE DB MDAC см.</span><span class="sxs-lookup"><span data-stu-id="ec25f-116">For more information about supported features with the Microsoft OLE DB Provider for ODBC, the Microsoft OLE DB Provider for Oracle, or the Microsoft SQL Server OLE DB Provider, see the MDAC readme file.</span></span>

<span data-ttu-id="ec25f-117">В этом документе предполагается разобраться в Microsoft Visual Basic® программирования языка и общие знания ADO.</span><span class="sxs-lookup"><span data-stu-id="ec25f-117">This document assumes a working knowledge of the Microsoft® Visual Basic® programming language and a general knowledge of ADO.</span></span> <span data-ttu-id="ec25f-118">Дополнительные сведения о ADO [Руководство программиста ADO](ado-programmer-s-guide.md)см.</span><span class="sxs-lookup"><span data-stu-id="ec25f-118">For more information about ADO, see the [ADO Programmer's Guide](ado-programmer-s-guide.md).</span></span> <span data-ttu-id="ec25f-119">Для получения дополнительных сведений о ADOX в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="ec25f-119">For more overview information about ADOX, see the following topics:</span></span>

  - [<span data-ttu-id="ec25f-120">ADOX Objects</span><span class="sxs-lookup"><span data-stu-id="ec25f-120">ADOX Objects</span></span>](adox-objects.md)

  - [<span data-ttu-id="ec25f-121">ADOX Collections</span><span class="sxs-lookup"><span data-stu-id="ec25f-121">ADOX Collections</span></span>](adox-collections.md)

  - [<span data-ttu-id="ec25f-122">ADOX Properties</span><span class="sxs-lookup"><span data-stu-id="ec25f-122">ADOX Properties</span></span>](adox-properties.md)

  - [<span data-ttu-id="ec25f-123">ADOX Methods</span><span class="sxs-lookup"><span data-stu-id="ec25f-123">ADOX Methods</span></span>](adox-methods.md)

  - [<span data-ttu-id="ec25f-124">Примеры ADOX</span><span class="sxs-lookup"><span data-stu-id="ec25f-124">ADOX Examples</span></span>](adox-code-examples.md)

