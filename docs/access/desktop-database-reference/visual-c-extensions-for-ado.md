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
# <a name="visual-c-extensions-for-ado"></a><span data-ttu-id="31fe5-102">Расширения Visual C++ для ADO</span><span class="sxs-lookup"><span data-stu-id="31fe5-102">Visual C++ Extensions for ADO</span></span>


<span data-ttu-id="31fe5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31fe5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31fe5-104">Предпочтительным методом программирования ADO с **\#** Visual C++ является использование директивы импорта, как это Microsoft Visual C++ [ADO Programming.](visual-c-ado-programming.md)</span><span class="sxs-lookup"><span data-stu-id="31fe5-104">The preferred method of programming ADO with Visual C++ is using the **\#import** directive, as discussed in [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md).</span></span> <span data-ttu-id="31fe5-105">Однако более ранние версии ADO поставляются с альтернативным методом программирования с помощью Visual C++: Visual C++ Extensions.</span><span class="sxs-lookup"><span data-stu-id="31fe5-105">However, earlier versions of ADO shipped with an alternate method of programming using Visual C++: the Visual C++ Extensions.</span></span> <span data-ttu-id="31fe5-106">В этом разделе документируется эта функция для тех, кто должен поддерживать код расширений Visual C++, но новый код ADO должен быть написан с помощью \# **импорта.**</span><span class="sxs-lookup"><span data-stu-id="31fe5-106">This section documents this feature for those who must maintain Visual C++ Extensions code, but new ADO code should be written using \#**import**.</span></span>

<span data-ttu-id="31fe5-107">Одна из самых утомительных задач, с чем сталкиваются программисты Visual C++ при сборе данных с помощью ADO, — преобразование данных, возвращающихся в виде типа данных VARIANT, в тип данных C++, а затем хранение преобразованных данных в классе или структуре.</span><span class="sxs-lookup"><span data-stu-id="31fe5-107">One of the most tedious jobs Visual C++ programmers face when retrieving data with ADO is converting data returned as a VARIANT data type into a C++ data type, and then storing the converted data in a class or structure.</span></span> <span data-ttu-id="31fe5-108">В дополнение к тому, что они являются громоздкими, сбор данных C++ с помощью типа данных VARIANT снижает производительность.</span><span class="sxs-lookup"><span data-stu-id="31fe5-108">In addition to being cumbersome, retrieving C++ data through a VARIANT data type diminishes performance.</span></span>

<span data-ttu-id="31fe5-109">ADO предоставляет интерфейс, который поддерживает сбор данных в родные типы данных C/C++ без использования VARIANT, а также макрос предпроцессора, упрощающий использование интерфейса.</span><span class="sxs-lookup"><span data-stu-id="31fe5-109">ADO provides an interface that supports retrieving data into native C/C++ data types without going through a VARIANT, and also provides preprocessor macros that simplify using the interface.</span></span> <span data-ttu-id="31fe5-110">В результате это гибкий инструмент, который проще в использовании и имеет большую производительность.</span><span class="sxs-lookup"><span data-stu-id="31fe5-110">The result is a flexible tool that is easier to use and has great performance.</span></span>

<span data-ttu-id="31fe5-111">Распространенный клиентский сценарий C/C++ — привязка записи в [Наборе](recordset-object-ado.md) записей к структуре C/C++ или классу, содержащим родные типы C/C++.</span><span class="sxs-lookup"><span data-stu-id="31fe5-111">A common C/C++ client scenario is to bind a record in a [Recordset](recordset-object-ado.md) to a C/C++ struct or class containing native C/C++ types.</span></span> <span data-ttu-id="31fe5-112">При переходе на VARIANTs это включает написание кода преобразования из VARIANT в типы C/C++ .</span><span class="sxs-lookup"><span data-stu-id="31fe5-112">When going through VARIANTs, this involves writing conversion code from VARIANT to C/C++ native types.</span></span> <span data-ttu-id="31fe5-113">Расширение Visual C++ для ADO нацелено на то, чтобы значительно упростить этот сценарий для программиста Visual C++.</span><span class="sxs-lookup"><span data-stu-id="31fe5-113">The Visual C++ Extensions for ADO are targeted at making this scenario much easier for the Visual C++ programmer.</span></span>

<span data-ttu-id="31fe5-114">Дополнительные разделы о расширении Visual C++ для ADO см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="31fe5-114">See the following topics to learn more about the Visual C++ Extensions for ADO.</span></span>

  - [<span data-ttu-id="31fe5-115">Использование расширений Visual C++ для ADO</span><span class="sxs-lookup"><span data-stu-id="31fe5-115">Using Visual C++ Extensions for ADO</span></span>](using-visual-c-extensions.md)

  - [<span data-ttu-id="31fe5-116">Visual C++ Extensions Header</span><span class="sxs-lookup"><span data-stu-id="31fe5-116">Visual C++ Extensions Header</span></span>](visual-c-extensions-header.md)

  - [<span data-ttu-id="31fe5-117">Пример ADO с визуальными расширениями C++</span><span class="sxs-lookup"><span data-stu-id="31fe5-117">ADO with Visual C++ Extensions Example</span></span>](visual-c-extensions-example.md)

