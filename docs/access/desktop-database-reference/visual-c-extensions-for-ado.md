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
# <a name="visual-c-extensions-for-ado"></a><span data-ttu-id="8a0e7-102">Расширения Visual C++ для ADO</span><span class="sxs-lookup"><span data-stu-id="8a0e7-102">Visual C++ Extensions for ADO</span></span>


<span data-ttu-id="8a0e7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a0e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8a0e7-104">Предпочтительный метод программирования ADO в Visual C++ использует директиву \*\* \#Import\*\* , как описано в разделе [программирование ADO на Microsoft Visual c++](visual-c-ado-programming.md).</span><span class="sxs-lookup"><span data-stu-id="8a0e7-104">The preferred method of programming ADO with Visual C++ is using the **\#import** directive, as discussed in [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md).</span></span> <span data-ttu-id="8a0e7-105">Однако более ранние версии ADO поставляются с альтернативным способом программирования с использованием Visual C++: расширения Visual C++.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-105">However, earlier versions of ADO shipped with an alternate method of programming using Visual C++: the Visual C++ Extensions.</span></span> <span data-ttu-id="8a0e7-106">В этом разделе описана эта функция для тех, кто должен поддерживать код расширений Visual C++, но новый код ADO должен \#быть написан с помощью метода **Import**.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-106">This section documents this feature for those who must maintain Visual C++ Extensions code, but new ADO code should be written using \#**import**.</span></span>

<span data-ttu-id="8a0e7-107">Один из самых трудоемких задач программистов Visual C++ при получении данных с помощью ADO преобразует данные, возвращаемые в тип данных VARIANT, в тип данных C++, а затем сохраняет преобразованные данные в классе или структуре.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-107">One of the most tedious jobs Visual C++ programmers face when retrieving data with ADO is converting data returned as a VARIANT data type into a C++ data type, and then storing the converted data in a class or structure.</span></span> <span data-ttu-id="8a0e7-108">Помимо громоздких, извлечение данных C++ через тип данных VARIANT уменьшает производительность.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-108">In addition to being cumbersome, retrieving C++ data through a VARIANT data type diminishes performance.</span></span>

<span data-ttu-id="8a0e7-109">ADO предоставляет интерфейс, который поддерживает извлечение данных в собственные типы данных C/C++ без прохода по типу VARIANT, а также предоставляет макрос препроцессора, который упрощает использование интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-109">ADO provides an interface that supports retrieving data into native C/C++ data types without going through a VARIANT, and also provides preprocessor macros that simplify using the interface.</span></span> <span data-ttu-id="8a0e7-110">Результатом является гибкое средство, которое проще в использовании и обладает высокой производительностью.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-110">The result is a flexible tool that is easier to use and has great performance.</span></span>

<span data-ttu-id="8a0e7-111">Распространенным сценарием для клиента C/C++ является привязка записи в объекте [Recordset](recordset-object-ado.md) К структуре C/c++ или классу, содержащему собственные типы C/c++.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-111">A common C/C++ client scenario is to bind a record in a [Recordset](recordset-object-ado.md) to a C/C++ struct or class containing native C/C++ types.</span></span> <span data-ttu-id="8a0e7-112">При переходе по вариантам это включает в себя написание кода преобразования из VARIANT в собственные типы C/C++.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-112">When going through VARIANTs, this involves writing conversion code from VARIANT to C/C++ native types.</span></span> <span data-ttu-id="8a0e7-113">Расширения Visual C++ для ADO предназначены для значительного упрощения этого сценария в Visual C++ программиста.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-113">The Visual C++ Extensions for ADO are targeted at making this scenario much easier for the Visual C++ programmer.</span></span>

<span data-ttu-id="8a0e7-114">Чтобы узнать больше о расширениях Visual C++ для ADO, ознакомьтесь со следующими статьями.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-114">See the following topics to learn more about the Visual C++ Extensions for ADO.</span></span>

  - [<span data-ttu-id="8a0e7-115">Использование расширений Visual C++ для ADO</span><span class="sxs-lookup"><span data-stu-id="8a0e7-115">Using Visual C++ Extensions for ADO</span></span>](using-visual-c-extensions.md)

  - [<span data-ttu-id="8a0e7-116">Visual C++ Extensions Header</span><span class="sxs-lookup"><span data-stu-id="8a0e7-116">Visual C++ Extensions Header</span></span>](visual-c-extensions-header.md)

  - [<span data-ttu-id="8a0e7-117">Пример расширений ADO с использованием расширений Visual C++</span><span class="sxs-lookup"><span data-stu-id="8a0e7-117">ADO with Visual C++ Extensions Example</span></span>](visual-c-extensions-example.md)

