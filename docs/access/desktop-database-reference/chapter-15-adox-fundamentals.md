---
title: Глава 15. Основы ADOX
TOCTitle: 'Chapter 15: ADOX fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e46920ba47dba018944768ff61c970781e37a02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296453"
---
# <a name="chapter-15-adox-fundamentals"></a><span data-ttu-id="fcc8a-102">Глава 15. Основы ADOX</span><span class="sxs-lookup"><span data-stu-id="fcc8a-102">Chapter 15: ADOX fundamentals</span></span>

<span data-ttu-id="fcc8a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcc8a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fcc8a-104">Расширения объектов данных Microsoft ActiveX для языка определения данных и безопасности (ADOX) являются расширением объектов ADO и программной модели.</span><span class="sxs-lookup"><span data-stu-id="fcc8a-104">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model.</span></span> <span data-ttu-id="fcc8a-105">ADOX включает объекты для создания и изменения схемы, а также для обеспечения безопасности.</span><span class="sxs-lookup"><span data-stu-id="fcc8a-105">ADOX includes objects for schema creation and modification, as well as security.</span></span> <span data-ttu-id="fcc8a-106">Так как это подход, основанный на объектах, для управления схемой, вы можете написать код, который будет работать с разными источниками данных независимо от различий в их исходных синтаксисах.</span><span class="sxs-lookup"><span data-stu-id="fcc8a-106">Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="fcc8a-107">ADOX — вспомогательная библиотека для базовых объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="fcc8a-107">ADOX is a companion library to the core ADO objects.</span></span> <span data-ttu-id="fcc8a-108">Он предоставляет доступ к дополнительным объектам для создания, изменения и удаления объектов схемы, таких как таблицы и процедуры.</span><span class="sxs-lookup"><span data-stu-id="fcc8a-108">It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures.</span></span> <span data-ttu-id="fcc8a-109">Он также включает объекты безопасности для поддержки пользователей и групп, а также для предоставления и отзыва разрешений на объекты.</span><span class="sxs-lookup"><span data-stu-id="fcc8a-109">It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

<span data-ttu-id="fcc8a-110">Чтобы использовать ADOX с вашим средством разработки, необходимо создать ссылку на библиотеку типов ADOX.</span><span class="sxs-lookup"><span data-stu-id="fcc8a-110">To use ADOX with your development tool, you should establish a reference to the ADOX type library.</span></span> <span data-ttu-id="fcc8a-111">Описание библиотеки ADOX: "Microsoft ADO ext. для DDL и безопасности".</span><span class="sxs-lookup"><span data-stu-id="fcc8a-111">The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security."</span></span> <span data-ttu-id="fcc8a-112">Имя файла библиотеки ADOX — Мсадокс. dll, а идентификатор программы (ProgID) — "ADOX".</span><span class="sxs-lookup"><span data-stu-id="fcc8a-112">The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX".</span></span> <span data-ttu-id="fcc8a-113">Для получения дополнительных сведений об установке ссылок на библиотеки, ознакомьтесь с документацией по средству разработки.</span><span class="sxs-lookup"><span data-stu-id="fcc8a-113">For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="fcc8a-114">Поставщик Microsoft OLE DB для ядра базы данных Microsoft Jet полностью поддерживает ADOX.</span><span class="sxs-lookup"><span data-stu-id="fcc8a-114">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX.</span></span> <span data-ttu-id="fcc8a-115">Некоторые функции ADOX могут не поддерживаться в зависимости от поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="fcc8a-115">Certain features of ADOX may not be supported, depending on your data provider.</span></span> <span data-ttu-id="fcc8a-116">Дополнительные сведения о поддерживаемых возможностях с помощью поставщика Microsoft OLE DB для ODBC, поставщика Microsoft OLE DB для Oracle или поставщика OLE DB для Microsoft SQL Server можно найти в файле readme MDAC.</span><span class="sxs-lookup"><span data-stu-id="fcc8a-116">For more information about supported features with the Microsoft OLE DB Provider for ODBC, the Microsoft OLE DB Provider for Oracle, or the Microsoft SQL Server OLE DB Provider, see the MDAC readme file.</span></span>

<span data-ttu-id="fcc8a-117">В этом документе предполагается работа со сведениями о языке программирования Microsoft Visual Basic и общие сведения об ADO.</span><span class="sxs-lookup"><span data-stu-id="fcc8a-117">This document assumes a working knowledge of the Microsoft Visual Basic programming language and a general knowledge of ADO.</span></span> <span data-ttu-id="fcc8a-118">Более подробную информацию об ADO можно узнать в [руководстве программиста по ADO](ado-programmer-s-guide.md).</span><span class="sxs-lookup"><span data-stu-id="fcc8a-118">For more information about ADO, see the [ADO programmer's guide](ado-programmer-s-guide.md).</span></span>

<span data-ttu-id="fcc8a-119">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="fcc8a-119">This chapter covers the following topic:</span></span>

- [<span data-ttu-id="fcc8a-120">Поддержка поставщиков для ADOX</span><span class="sxs-lookup"><span data-stu-id="fcc8a-120">Provider support for ADOX</span></span>](provider-support-for-adox.md)

<span data-ttu-id="fcc8a-121">Дополнительные сведения о ADOX см в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="fcc8a-121">For more overview information about ADOX, see the following topics:</span></span>

- [<span data-ttu-id="fcc8a-122">Объекты ADOX</span><span class="sxs-lookup"><span data-stu-id="fcc8a-122">ADOX objects</span></span>](adox-objects.md)
- [<span data-ttu-id="fcc8a-123">Коллекции ADOX</span><span class="sxs-lookup"><span data-stu-id="fcc8a-123">ADOX collections</span></span>](adox-collections.md)
- [<span data-ttu-id="fcc8a-124">Свойства ADOX</span><span class="sxs-lookup"><span data-stu-id="fcc8a-124">ADOX properties</span></span>](adox-properties.md)
- [<span data-ttu-id="fcc8a-125">Методы ADOX</span><span class="sxs-lookup"><span data-stu-id="fcc8a-125">ADOX methods</span></span>](adox-methods.md)
- [<span data-ttu-id="fcc8a-126">Примеры ADOX</span><span class="sxs-lookup"><span data-stu-id="fcc8a-126">ADOX examples</span></span>](adox-code-examples.md)

