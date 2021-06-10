---
title: Программирование ADO/WFC
TOCTitle: ADO/WFC programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 904b5e3930c0e7e7b1d98f94bd39cfbf816aa145
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283207"
---
# <a name="adowfc-programming"></a><span data-ttu-id="2bb07-102">Программирование ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2bb07-102">ADO/WFC programming</span></span>

<span data-ttu-id="2bb07-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2bb07-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2bb07-104">Для Microsoft Visual J++ 6.0 ADO была расширена для работы с Windows классами фонда (WFC) следующими способами.</span><span class="sxs-lookup"><span data-stu-id="2bb07-104">For Microsoft Visual J++ 6.0, ADO has been extended to work with Windows Foundation Classes (WFC) in the following ways.</span></span> <span data-ttu-id="2bb07-105">Во-первых, реализован набор классов Java, который расширяет интерфейсы ADO и создает уведомления, интересные программисту Java; Классы Java также раскрывают функции, возвращая типы Java пользователю.</span><span class="sxs-lookup"><span data-stu-id="2bb07-105">First, a set of Java classes has been implemented that extends the ADO interfaces and creates notifications interesting to the Java programmer; the Java classes also expose functions that return Java types to the user.</span></span> <span data-ttu-id="2bb07-106">Чтобы повысить производительность, класс Java напрямую имеет доступ к родным типам данных в объекте rowset OLE DB и возвращает их программисту Java в качестве типов Java, не преобразовав их в вариант и из него.</span><span class="sxs-lookup"><span data-stu-id="2bb07-106">To improve performance, the Java class directly accesses the native data types in the OLE DB rowset object, and returns them to the Java programmer as Java types without first converting them to and from a variant.</span></span> <span data-ttu-id="2bb07-107">ADO также расширена для работы с уведомлениями о событиях в рамках WFC.</span><span class="sxs-lookup"><span data-stu-id="2bb07-107">ADO has also been extended to work with event notifications in the WFC framework.</span></span>

<span data-ttu-id="2bb07-108">ADO для Windows классов Foundation (ADO/WFC) поддерживает все стандартные методы ADO, свойства, объекты и события.</span><span class="sxs-lookup"><span data-stu-id="2bb07-108">ADO for Windows Foundation Classes (ADO/WFC) supports all the standard ADO methods, properties, objects, and events.</span></span> <span data-ttu-id="2bb07-109">Однако операции, которые требуют варианта в качестве параметра и демонстрируют отличную производительность на таком языке, как Microsoft Visual Basic, отображают меньшую производительность на языке, например Visual J++.</span><span class="sxs-lookup"><span data-stu-id="2bb07-109">However, operations that require a variant as a parameter and show excellent performance in a language such as Microsoft Visual Basic, display lesser performance in a language such as Visual J++.</span></span> <span data-ttu-id="2bb07-110">По этой причине ADO/WFC также предоставляет вспомогательные функции на [объекте Field,](field-object-ado.md) который принимает родные типы данных Java, а не тип данных вариантов.</span><span class="sxs-lookup"><span data-stu-id="2bb07-110">For that reason, ADO/WFC also provides accessor functions on the [Field](field-object-ado.md) object that take native Java data types instead of the variant data type.</span></span>

<span data-ttu-id="2bb07-111">Дополнительные сведения в документации ADO о пакетах ADO/WFC см. в индексе [синтаксиса ADO/WFC.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index)</span><span class="sxs-lookup"><span data-stu-id="2bb07-111">For more detailed information within the ADO documentation about ADO/WFC packages, see [the ADO/WFC Syntax Index](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index).</span></span>

## <a name="referencing-the-library"></a><span data-ttu-id="2bb07-112">Ссылки на библиотеку</span><span class="sxs-lookup"><span data-stu-id="2bb07-112">Referencing the library</span></span>

<span data-ttu-id="2bb07-113">Чтобы импортировать классы данных ADO/WFC в проект, включите в код следующую строку:</span><span class="sxs-lookup"><span data-stu-id="2bb07-113">To import the ADO/WFC data classes into your project, include the following line in your code:</span></span>

```java 
 
import com.ms.wfc.data.*; 
```

