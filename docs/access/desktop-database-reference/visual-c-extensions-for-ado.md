---
title: Расширения Visual C++ для ADO
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fc69d3244cf6faf3aa91fe954e4b39323cf13abf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302756"
---
# <a name="visual-c-extensions-for-ado"></a><span data-ttu-id="474b0-102">Расширения Visual C++ для ADO</span><span class="sxs-lookup"><span data-stu-id="474b0-102">Visual C++ Extensions for ADO</span></span>


<span data-ttu-id="474b0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="474b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="474b0-104">Предпочтительным методом программирования ADO с **\#** visual C++ является использование директивы импорта, как было рассмотрено в microsoft [Visual C++ ADO Programming.](visual-c-ado-programming.md)</span><span class="sxs-lookup"><span data-stu-id="474b0-104">The preferred method of programming ADO with Visual C++ is using the **\#import** directive, as discussed in [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md).</span></span> <span data-ttu-id="474b0-105">Однако более ранние версии ADO поставлялись с альтернативным методом программирования с использованием Visual C++: расширения Visual C++.</span><span class="sxs-lookup"><span data-stu-id="474b0-105">However, earlier versions of ADO shipped with an alternate method of programming using Visual C++: the Visual C++ Extensions.</span></span> <span data-ttu-id="474b0-106">В этом разделе документируется эта функция для тех, кто должен поддерживать код расширений Visual C++, но новый код ADO должен быть написан с помощью \# **импорта**.</span><span class="sxs-lookup"><span data-stu-id="474b0-106">This section documents this feature for those who must maintain Visual C++ Extensions code, but new ADO code should be written using \#**import**.</span></span>

<span data-ttu-id="474b0-107">Одно из самых утомительных заданий, с чем сталкиваются программисты Visual C++ при возвращении данных с помощью ADO, — преобразование данных, возвращаемого в виде типа данных VARIANT, в тип данных C++, а затем сохранение преобразованных данных в классе или структуре.</span><span class="sxs-lookup"><span data-stu-id="474b0-107">One of the most tedious jobs Visual C++ programmers face when retrieving data with ADO is converting data returned as a VARIANT data type into a C++ data type, and then storing the converted data in a class or structure.</span></span> <span data-ttu-id="474b0-108">Помимо того, что процесс является слишком утомительным, искомые данные C++ с помощью типа данных VARIANT снижают производительность.</span><span class="sxs-lookup"><span data-stu-id="474b0-108">In addition to being cumbersome, retrieving C++ data through a VARIANT data type diminishes performance.</span></span>

<span data-ttu-id="474b0-109">ADO предоставляет интерфейс, который поддерживает искомые данные в нативных типах данных C/C++ без использования VARIANT, а также содержит макрос предварительной обработки, упрощающий использование интерфейса.</span><span class="sxs-lookup"><span data-stu-id="474b0-109">ADO provides an interface that supports retrieving data into native C/C++ data types without going through a VARIANT, and also provides preprocessor macros that simplify using the interface.</span></span> <span data-ttu-id="474b0-110">Результатом является гибкое средство, которое проще в использовании и имеет большую производительность.</span><span class="sxs-lookup"><span data-stu-id="474b0-110">The result is a flexible tool that is easier to use and has great performance.</span></span>

<span data-ttu-id="474b0-111">Распространенный сценарий клиента C/C++ — привязка записи в наборе [записей](recordset-object-ado.md) к структуре C/C++ или классу, содержащей нативные типы C/C++.</span><span class="sxs-lookup"><span data-stu-id="474b0-111">A common C/C++ client scenario is to bind a record in a [Recordset](recordset-object-ado.md) to a C/C++ struct or class containing native C/C++ types.</span></span> <span data-ttu-id="474b0-112">При переходе через VARIANTs это включает написание кода преобразования из VARIANT в исходные типы C/C++.</span><span class="sxs-lookup"><span data-stu-id="474b0-112">When going through VARIANTs, this involves writing conversion code from VARIANT to C/C++ native types.</span></span> <span data-ttu-id="474b0-113">Расширения Visual C++ для ADO значительно упрощают этот сценарий для программиста Visual C++.</span><span class="sxs-lookup"><span data-stu-id="474b0-113">The Visual C++ Extensions for ADO are targeted at making this scenario much easier for the Visual C++ programmer.</span></span>

<span data-ttu-id="474b0-114">В следующих темах вы узнаете больше о расширениях Visual C++ для ADO.</span><span class="sxs-lookup"><span data-stu-id="474b0-114">See the following topics to learn more about the Visual C++ Extensions for ADO.</span></span>

  - [<span data-ttu-id="474b0-115">Использование расширений Visual C++ для ADO</span><span class="sxs-lookup"><span data-stu-id="474b0-115">Using Visual C++ Extensions for ADO</span></span>](using-visual-c-extensions.md)

  - [<span data-ttu-id="474b0-116">Visual C++ Extensions Header</span><span class="sxs-lookup"><span data-stu-id="474b0-116">Visual C++ Extensions Header</span></span>](visual-c-extensions-header.md)

  - [<span data-ttu-id="474b0-117">ADO with Visual C++ Extensions Example</span><span class="sxs-lookup"><span data-stu-id="474b0-117">ADO with Visual C++ Extensions Example</span></span>](visual-c-extensions-example.md)

