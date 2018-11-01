---
title: Программирование ADO/WFC
TOCTitle: ADO/WFC Programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea531f484ad75de268f0d4fb38a10e617c1851e6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884634"
---
# <a name="adowfc-programming"></a><span data-ttu-id="7f0a7-102">Программирование ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="7f0a7-102">ADO/WFC Programming</span></span>


<span data-ttu-id="7f0a7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f0a7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f0a7-104">Для Microsoft Visual J ++ 6.0 ADO расширен для работы с Windows Foundation классы (WFC) следующим образом.</span><span class="sxs-lookup"><span data-stu-id="7f0a7-104">For Microsoft Visual J++ 6.0, ADO has been extended to work with Windows Foundation Classes (WFC) in the following ways.</span></span> <span data-ttu-id="7f0a7-105">Во-первых набор классов Java был реализован, который расширяет интерфейс ADO и создает уведомления интересно программиста Java; классы Java также предоставляют функции, которые возвращают типы Java для пользователя.</span><span class="sxs-lookup"><span data-stu-id="7f0a7-105">First, a set of Java classes has been implemented that extends the ADO interfaces and creates notifications interesting to the Java programmer; the Java classes also expose functions that return Java types to the user.</span></span> <span data-ttu-id="7f0a7-106">В целях повышения производительности класс Java непосредственно обращается к собственных типов данных в объекте набор строк OLE DB и возвращает их программисту Java как типы Java без предварительного преобразования их в и из него переменную типа variant.</span><span class="sxs-lookup"><span data-stu-id="7f0a7-106">To improve performance, the Java class directly accesses the native data types in the OLE DB rowset object, and returns them to the Java programmer as Java types without first converting them to and from a variant.</span></span> <span data-ttu-id="7f0a7-107">Также была расширена ADO для работы с уведомления о событиях в платформе WFC.</span><span class="sxs-lookup"><span data-stu-id="7f0a7-107">ADO has also been extended to work with event notifications in the WFC framework.</span></span>

<span data-ttu-id="7f0a7-108">ADO для Windows классов (ADO/WFC) поддерживает все стандартные ADO методы, свойства, объектов и событий.</span><span class="sxs-lookup"><span data-stu-id="7f0a7-108">ADO for Windows Foundation Classes (ADO/WFC) supports all the standard ADO methods, properties, objects, and events.</span></span> <span data-ttu-id="7f0a7-109">Тем не менее операции, которые требуют вариант в качестве параметра и отображение высокая производительность на языке, такие как Microsoft Visual Basic, отображение снижения производительности на языке, например Visual J ++.</span><span class="sxs-lookup"><span data-stu-id="7f0a7-109">However, operations that require a variant as a parameter and show excellent performance in a language such as Microsoft Visual Basic, display lesser performance in a language such as Visual J++.</span></span> <span data-ttu-id="7f0a7-110">По этой причине ADO/WFC также предоставляет функции для доступа к данным на объект [поля](field-object-ado.md) , вступили в собственных типов данных Java вместо тип данных variant.</span><span class="sxs-lookup"><span data-stu-id="7f0a7-110">For that reason, ADO/WFC also provides accessor functions on the [Field](field-object-ado.md) object that take native Java data types instead of the variant data type.</span></span>

<span data-ttu-id="7f0a7-111">Для получения дополнительных сведений в ADO документацию о пакетах ADO/WFC [ADO/WFC синтаксис](https://msdn.microsoft.com/library/jj250066\(v=office.15\))см.</span><span class="sxs-lookup"><span data-stu-id="7f0a7-111">For more detailed information within the ADO documentation about ADO/WFC packages, see [the ADO/WFC Syntax Index](https://msdn.microsoft.com/library/jj250066\(v=office.15\)).</span></span>

## <a name="referencing-the-library"></a><span data-ttu-id="7f0a7-112">Создание ссылок на библиотеку</span><span class="sxs-lookup"><span data-stu-id="7f0a7-112">Referencing the Library</span></span>

<span data-ttu-id="7f0a7-113">Для импорта классов данных ADO/WFC в проекте, необходимо включите следующую строку кода:</span><span class="sxs-lookup"><span data-stu-id="7f0a7-113">To import the ADO/WFC data classes into your project, include the following line in your code:</span></span>

```java 
 
import com.ms.wfc.data.*; 
```

