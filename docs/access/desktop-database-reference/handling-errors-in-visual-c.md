---
title: Обработка ошибок в Visual C++
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d0e76dc3cc9634a1531a34058bf7a1baf636c94c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292029"
---
# <a name="handling-errors-in-visual-c"></a><span data-ttu-id="70817-102">Обработка ошибок в Visual C++</span><span class="sxs-lookup"><span data-stu-id="70817-102">Handling errors in Visual C++</span></span>


<span data-ttu-id="70817-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70817-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70817-104">В COM большинство операций возвращают код возврата HRESULT, который указывает, успешно ли выполнена функция.</span><span class="sxs-lookup"><span data-stu-id="70817-104">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="70817-105">Директива \#импорта создает код обертки вокруг каждого "необработанного" метода или свойства и проверяет ВОЗВРАЩАЕМОЕ значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="70817-105">The \#import directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="70817-106">Если HRESULT указывает на ошибку, код оболочки создает ошибку COM, вызывая \_com-\_ошибку\_еррорекс () с возвращаемым кодом возврата HRESULT в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="70817-106">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="70817-107">Объекты ошибок COM можно перехватывать в блоке **try-catch** .</span><span class="sxs-lookup"><span data-stu-id="70817-107">COM error objects can be caught in a **try-catch** block.</span></span> <span data-ttu-id="70817-108">(Чтобы обеспечить эффективность, перехватите ссылку на объект \_Error\_com.)</span><span class="sxs-lookup"><span data-stu-id="70817-108">(For efficiency's sake, catch a reference to a \_com\_error object.)</span></span>

<span data-ttu-id="70817-109">Помните, что это ошибки ADO: они возникают при неисправности операции ADO.</span><span class="sxs-lookup"><span data-stu-id="70817-109">Remember, these are ADO errors: they result from the ADO operation failing.</span></span> <span data-ttu-id="70817-110">Ошибки, возвращенные базовым поставщиком, отображаются как объекты **Error** в коллекции **ошибок** объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="70817-110">Errors returned by the underlying provider appear as **Error** objects in the **Connection** object's **Errors** collection.</span></span>

<span data-ttu-id="70817-111">Директива \#import создает только процедуры обработки ошибок для методов и свойств, объявленных в ADO. dll.</span><span class="sxs-lookup"><span data-stu-id="70817-111">The \#import directive only creates error-handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="70817-112">Тем не менее, вы можете использовать такой же механизм обработки ошибок, написав собственный макрос или встроенную функцию проверки ошибок.</span><span class="sxs-lookup"><span data-stu-id="70817-112">However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</span></span> <span data-ttu-id="70817-113">В этом разделе приведены примеры расширений Visual C++.</span><span class="sxs-lookup"><span data-stu-id="70817-113">See the topic Visual C++ Extensions for examples.</span></span>

