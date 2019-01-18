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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720235"
---
# <a name="visual-c-extensions-for-ado"></a><span data-ttu-id="76216-102">Расширения Visual C++ для ADO</span><span class="sxs-lookup"><span data-stu-id="76216-102">Visual C++ Extensions for ADO</span></span>


<span data-ttu-id="76216-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76216-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76216-104">С помощью предпочтительным программирования ADO с помощью Visual C++ \*\* \#импорта\*\* директивы, как описано в [Microsoft Visual C++ ADO программирования](visual-c-ado-programming.md).</span><span class="sxs-lookup"><span data-stu-id="76216-104">The preferred method of programming ADO with Visual C++ is using the **\#import** directive, as discussed in [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md).</span></span> <span data-ttu-id="76216-105">Тем не менее, более ранних версий ADO в состав альтернативного метода программирование с использованием Visual C++: расширения Visual C++.</span><span class="sxs-lookup"><span data-stu-id="76216-105">However, earlier versions of ADO shipped with an alternate method of programming using Visual C++: the Visual C++ Extensions.</span></span> <span data-ttu-id="76216-106">В данном разделе описываются этой функции для тех, кто должен поддерживать код расширений Visual C++, но новый код ADO должны быть написаны с помощью \# **импорта**.</span><span class="sxs-lookup"><span data-stu-id="76216-106">This section documents this feature for those who must maintain Visual C++ Extensions code, but new ADO code should be written using \#**import**.</span></span>

<span data-ttu-id="76216-107">Одно из наиболее утомительные заданий Visual C++ с любым опытом вставлялись при получения данных с помощью ADO преобразование данных возвращаются как тип данных VARIANT в тип данных C++ и затем хранения преобразованные данные в класс или структуру.</span><span class="sxs-lookup"><span data-stu-id="76216-107">One of the most tedious jobs Visual C++ programmers face when retrieving data with ADO is converting data returned as a VARIANT data type into a C++ data type, and then storing the converted data in a class or structure.</span></span> <span data-ttu-id="76216-108">В дополнение к сложный, извлечение данных C++ через тип данных VARIANT снижает производительность.</span><span class="sxs-lookup"><span data-stu-id="76216-108">In addition to being cumbersome, retrieving C++ data through a VARIANT data type diminishes performance.</span></span>

<span data-ttu-id="76216-109">ADO предоставляет интерфейс, который поддерживает извлечения данных в собственных типов данных C/C++ без прохода через значение типа VARIANT, а также препроцессору макросы, которые упрощают с использованием интерфейса.</span><span class="sxs-lookup"><span data-stu-id="76216-109">ADO provides an interface that supports retrieving data into native C/C++ data types without going through a VARIANT, and also provides preprocessor macros that simplify using the interface.</span></span> <span data-ttu-id="76216-110">Результатом является гибкий инструмент, который имеет высокую производительность и простых в использовании.</span><span class="sxs-lookup"><span data-stu-id="76216-110">The result is a flexible tool that is easier to use and has great performance.</span></span>

<span data-ttu-id="76216-111">Типичные сценарии клиента C/C++ является привязка записи в [набор записей](recordset-object-ado.md) на C/C++ структуры или класса, содержащего собственным типам C/C++.</span><span class="sxs-lookup"><span data-stu-id="76216-111">A common C/C++ client scenario is to bind a record in a [Recordset](recordset-object-ado.md) to a C/C++ struct or class containing native C/C++ types.</span></span> <span data-ttu-id="76216-112">При перенаправлении через вариантов, это включает в себя написание кода преобразования из типа VARIANT к собственным типам C/C++.</span><span class="sxs-lookup"><span data-stu-id="76216-112">When going through VARIANTs, this involves writing conversion code from VARIANT to C/C++ native types.</span></span> <span data-ttu-id="76216-113">Расширения Visual C++ для ADO направлены на выполнение этого сценария намного легче для программистов Visual C++.</span><span class="sxs-lookup"><span data-stu-id="76216-113">The Visual C++ Extensions for ADO are targeted at making this scenario much easier for the Visual C++ programmer.</span></span>

<span data-ttu-id="76216-114">В следующих разделах для получения дополнительных сведений о расширений Visual C++ для ADO.</span><span class="sxs-lookup"><span data-stu-id="76216-114">See the following topics to learn more about the Visual C++ Extensions for ADO.</span></span>

  - [<span data-ttu-id="76216-115">С помощью расширений Visual C++ для ADO</span><span class="sxs-lookup"><span data-stu-id="76216-115">Using Visual C++ Extensions for ADO</span></span>](using-visual-c-extensions.md)

  - [<span data-ttu-id="76216-116">Заголовок расширений Visual C++</span><span class="sxs-lookup"><span data-stu-id="76216-116">Visual C++ Extensions Header</span></span>](visual-c-extensions-header.md)

  - [<span data-ttu-id="76216-117">ADO с примером расширения Visual C++</span><span class="sxs-lookup"><span data-stu-id="76216-117">ADO with Visual C++ Extensions Example</span></span>](visual-c-extensions-example.md)

