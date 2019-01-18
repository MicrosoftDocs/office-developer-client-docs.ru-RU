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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720508"
---
# <a name="adowfc-programming"></a><span data-ttu-id="2079d-102">Программирование ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2079d-102">ADO/WFC programming</span></span>

<span data-ttu-id="2079d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2079d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2079d-104">Для Microsoft Visual J ++ 6.0 ADO расширен для работы с Windows Foundation классы (WFC) следующим образом.</span><span class="sxs-lookup"><span data-stu-id="2079d-104">For Microsoft Visual J++ 6.0, ADO has been extended to work with Windows Foundation Classes (WFC) in the following ways.</span></span> <span data-ttu-id="2079d-105">Во-первых набор классов Java был реализован, который расширяет интерфейс ADO и создает уведомления интересно программиста Java; классы Java также предоставляют функции, которые возвращают типы Java для пользователя.</span><span class="sxs-lookup"><span data-stu-id="2079d-105">First, a set of Java classes has been implemented that extends the ADO interfaces and creates notifications interesting to the Java programmer; the Java classes also expose functions that return Java types to the user.</span></span> <span data-ttu-id="2079d-106">В целях повышения производительности класс Java непосредственно обращается к собственных типов данных в объекте набор строк OLE DB и возвращает их программисту Java как типы Java без предварительного преобразования их в и из него переменную типа variant.</span><span class="sxs-lookup"><span data-stu-id="2079d-106">To improve performance, the Java class directly accesses the native data types in the OLE DB rowset object, and returns them to the Java programmer as Java types without first converting them to and from a variant.</span></span> <span data-ttu-id="2079d-107">Также была расширена ADO для работы с уведомления о событиях в платформе WFC.</span><span class="sxs-lookup"><span data-stu-id="2079d-107">ADO has also been extended to work with event notifications in the WFC framework.</span></span>

<span data-ttu-id="2079d-108">ADO для Windows классов (ADO/WFC) поддерживает все стандартные ADO методы, свойства, объектов и событий.</span><span class="sxs-lookup"><span data-stu-id="2079d-108">ADO for Windows Foundation Classes (ADO/WFC) supports all the standard ADO methods, properties, objects, and events.</span></span> <span data-ttu-id="2079d-109">Тем не менее операции, которые требуют вариант в качестве параметра и отображение высокая производительность на языке, такие как Microsoft Visual Basic, отображение снижения производительности на языке, например Visual J ++.</span><span class="sxs-lookup"><span data-stu-id="2079d-109">However, operations that require a variant as a parameter and show excellent performance in a language such as Microsoft Visual Basic, display lesser performance in a language such as Visual J++.</span></span> <span data-ttu-id="2079d-110">По этой причине ADO/WFC также предоставляет функции для доступа к данным на объект [поля](field-object-ado.md) , вступили в собственных типов данных Java вместо тип данных variant.</span><span class="sxs-lookup"><span data-stu-id="2079d-110">For that reason, ADO/WFC also provides accessor functions on the [Field](field-object-ado.md) object that take native Java data types instead of the variant data type.</span></span>

<span data-ttu-id="2079d-111">Для получения дополнительных сведений в ADO документацию о пакетах ADO/WFC [ADO/WFC синтаксис](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index)см.</span><span class="sxs-lookup"><span data-stu-id="2079d-111">For more detailed information within the ADO documentation about ADO/WFC packages, see [the ADO/WFC Syntax Index](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index).</span></span>

## <a name="referencing-the-library"></a><span data-ttu-id="2079d-112">Создание ссылок на библиотеку</span><span class="sxs-lookup"><span data-stu-id="2079d-112">Referencing the library</span></span>

<span data-ttu-id="2079d-113">Для импорта классов данных ADO/WFC в проекте, необходимо включите следующую строку кода:</span><span class="sxs-lookup"><span data-stu-id="2079d-113">To import the ADO/WFC data classes into your project, include the following line in your code:</span></span>

```java 
 
import com.ms.wfc.data.*; 
```

