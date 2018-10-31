---
title: Глава 14. Основные сведения об ADO MD
TOCTitle: 'Chapter 14: ADO MD Fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8576d2a1d579de306b438f7b0fb04a1eb2d46cc
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863652"
---
# <a name="chapter-14-ado-md-fundamentals"></a><span data-ttu-id="efcd8-102">Глава 14. Основные сведения об ADO MD</span><span class="sxs-lookup"><span data-stu-id="efcd8-102">Chapter 14: ADO MD Fundamentals</span></span>


<span data-ttu-id="efcd8-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="efcd8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="efcd8-104">Microsoft ActiveX Data Objects (ADO MD) (многомерные) обеспечивает быстрый доступ к многомерным данным из языков, такие как Microsoft Visual Basic, Microsoft Visual C++ и Microsoft Visual J ++.</span><span class="sxs-lookup"><span data-stu-id="efcd8-104">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++.</span></span> <span data-ttu-id="efcd8-105">ADO MD расширяет возможности Microsoft ActiveX Data Objects (ADO) для включения объектов, относящихся к многомерных данных, таких как объекты [CubeDef](cubedef-object-ado-md.md) и [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="efcd8-105">ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the [CubeDef](cubedef-object-ado-md.md) and [Cellset](cellset-object-ado-md.md) objects.</span></span> <span data-ttu-id="efcd8-106">С помощью ADO MD можно выбрать многомерные схему, запроса куба и получения результатов.</span><span class="sxs-lookup"><span data-stu-id="efcd8-106">With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="efcd8-107">Как и ADO ADO MD использует поставщика OLE DB для получения доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="efcd8-107">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data.</span></span> <span data-ttu-id="efcd8-108">Для работы с ADO MD, поставщик должен быть многомерные данные поставщика (MDP), определенный спецификации OLE DB для OLAP.</span><span class="sxs-lookup"><span data-stu-id="efcd8-108">To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification.</span></span> <span data-ttu-id="efcd8-109">MDPs представления данных в отличие от поставщиков табличных данных (за) многомерные представлениях, представляющих данные в табличных представлений.</span><span class="sxs-lookup"><span data-stu-id="efcd8-109">MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views.</span></span> <span data-ttu-id="efcd8-110">Обратитесь к документации для поставщика OLE DB для OLAP более подробные сведения о конкретных синтаксис и поведение поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="efcd8-110">Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

<span data-ttu-id="efcd8-111">В этом документе предполагается знание языка программирования Visual Basic и общие знания ADO и OLAP.</span><span class="sxs-lookup"><span data-stu-id="efcd8-111">This document assumes a working knowledge of the Visual Basic programming language and a general knowledge of ADO and OLAP.</span></span> <span data-ttu-id="efcd8-112">Для получения дополнительных сведений см. [Руководство программиста ADO](ado-programmer-s-guide.md) и OLE DB для OLAP программиста ссылку.</span><span class="sxs-lookup"><span data-stu-id="efcd8-112">For more information, see the [ADO Programmer's Guide](ado-programmer-s-guide.md) and the OLE DB for OLAP Programmer's Reference.</span></span> 

<span data-ttu-id="efcd8-113">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="efcd8-113">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="efcd8-114">Общие сведения о многомерных схемах и данных</span><span class="sxs-lookup"><span data-stu-id="efcd8-114">Overview of Multidimensional Schemas and Data</span></span>](overview-of-multidimensional-schemas-and-data.md)

- [<span data-ttu-id="efcd8-115">Работа с многомерными данными</span><span class="sxs-lookup"><span data-stu-id="efcd8-115">Working with Multidimensional Data</span></span>](working-with-multidimensional-data.md)

- [<span data-ttu-id="efcd8-116">Использование ADO с ADO MD</span><span class="sxs-lookup"><span data-stu-id="efcd8-116">Using ADO with ADO MD</span></span>](using-ado-with-ado-md.md)

- [<span data-ttu-id="efcd8-117">Программирование с помощью ADO MD</span><span class="sxs-lookup"><span data-stu-id="efcd8-117">Programming with ADO MD</span></span>](programming-with-ado-md.md)
