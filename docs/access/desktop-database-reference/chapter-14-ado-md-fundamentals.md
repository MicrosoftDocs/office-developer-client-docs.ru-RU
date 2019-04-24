---
title: Глава 14. Основы ADO MD
TOCTitle: 'Chapter 14: ADO MD fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44a4e666fb615f7d3870acfbd986e93971606d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296467"
---
# <a name="chapter-14-ado-md-fundamentals"></a><span data-ttu-id="df85a-102">Глава 14. Основы ADO MD</span><span class="sxs-lookup"><span data-stu-id="df85a-102">Chapter 14: ADO MD fundamentals</span></span>

<span data-ttu-id="df85a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df85a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df85a-104">Объекты данных Microsoft ActiveX (многомерные) (ADO MD) обеспечивают простой доступ к многомерным данным из таких языков, как Microsoft Visual Basic, Microsoft Visual C++ и Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="df85a-104">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++.</span></span> <span data-ttu-id="df85a-105">ADO MD расширяет возможности ADO Data Objects (ADO) для включения объектов, относящихся к многомерным данным, таких как объекты [CubeDef](cubedef-object-ado-md.md) и набор [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="df85a-105">ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the [CubeDef](cubedef-object-ado-md.md) and [Cellset](cellset-object-ado-md.md) objects.</span></span> <span data-ttu-id="df85a-106">С помощью ADO MD можно просматривать многомерную схему, запрашивать куб и получать результаты.</span><span class="sxs-lookup"><span data-stu-id="df85a-106">With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="df85a-107">Как и в ADO, ADO MD использует поставщика OLE DB для получения доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="df85a-107">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data.</span></span> <span data-ttu-id="df85a-108">Для работы с ADO MD поставщик должен быть многомерным поставщиком данных (МДП), как определено в спецификации OLE DB для OLAP.</span><span class="sxs-lookup"><span data-stu-id="df85a-108">To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification.</span></span> <span data-ttu-id="df85a-109">Мдпс представляют данные в многомерных представлениях, а не в табличных поставщиках данных (Тдпс), которые представляют данные в табличных представлениях.</span><span class="sxs-lookup"><span data-stu-id="df85a-109">MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views.</span></span> <span data-ttu-id="df85a-110">Обратитесь к документации по поставщику OLE DB для OLAP для получения более подробных сведений о конкретном синтаксисе и возможностях, поддерживаемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="df85a-110">Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

<span data-ttu-id="df85a-111">В этом документе предполагается работа со сведениями о языке программирования Visual Basic и общие сведения об ADO и OLAP.</span><span class="sxs-lookup"><span data-stu-id="df85a-111">This document assumes a working knowledge of the Visual Basic programming language and a general knowledge of ADO and OLAP.</span></span> <span data-ttu-id="df85a-112">Для получения дополнительных сведений ознакомьтесь с [руководством программиста по ADO](ado-programmer-s-guide.md) и справочникОм по программированию для программиста для куба OLE.</span><span class="sxs-lookup"><span data-stu-id="df85a-112">For more information, see the [ADO programmer's guide](ado-programmer-s-guide.md) and the OLE DB for OLAP Programmer's Reference.</span></span> 

<span data-ttu-id="df85a-113">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="df85a-113">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="df85a-114">Обзор многомерных схем и данных</span><span class="sxs-lookup"><span data-stu-id="df85a-114">Overview of multidimensional schemas and data</span></span>](overview-of-multidimensional-schemas-and-data.md)
- [<span data-ttu-id="df85a-115">Работа с многомерными данными</span><span class="sxs-lookup"><span data-stu-id="df85a-115">Working with multidimensional data</span></span>](working-with-multidimensional-data.md)
- [<span data-ttu-id="df85a-116">Using ADO with ADO MD</span><span class="sxs-lookup"><span data-stu-id="df85a-116">Using ADO with ADO MD</span></span>](using-ado-with-ado-md.md)
- [<span data-ttu-id="df85a-117">Programming with ADO MD</span><span class="sxs-lookup"><span data-stu-id="df85a-117">Programming with ADO MD</span></span>](programming-with-ado-md.md)
