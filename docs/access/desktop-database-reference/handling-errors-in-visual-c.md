---
title: Handling Errors in Visual C++
TOCTitle: Handling Errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f8feeb97e049d245da91371fdb5225a644d0e415
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480679"
---
# <a name="handling-errors-in-visual-c"></a><span data-ttu-id="52213-102">Handling Errors in Visual C++</span><span class="sxs-lookup"><span data-stu-id="52213-102">Handling Errors in Visual C++</span></span>


<span data-ttu-id="52213-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="52213-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="52213-104">В модели COM большинство операций возврата HRESULT кода возврата, которое указывает, будет ли функция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="52213-104">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="52213-105">\#Директива импорта создает код программы-оболочки вокруг каждого «необработанные» метод или свойство и проверяет возвращаемое значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="52213-105">The \#import directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="52213-106">Если значение HRESULT указывает на ошибку, кода программы-оболочки для вызывает ошибку COM путем вызова \_com\_проблему\_errorex() со значением HRESULT возвращают код в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="52213-106">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="52213-107">Ошибка COM-объектов может быть зафиксировано в блок **try-catch** .</span><span class="sxs-lookup"><span data-stu-id="52213-107">COM error objects can be caught in a **try-catch** block.</span></span> <span data-ttu-id="52213-108">(Ради повышения эффективности перехватывающей ссылку на \_com\_объект error.)</span><span class="sxs-lookup"><span data-stu-id="52213-108">(For efficiency's sake, catch a reference to a \_com\_error object.)</span></span>

<span data-ttu-id="52213-109">Помните, что это ADO ошибки: они являются результатом сбоя операции ADO.</span><span class="sxs-lookup"><span data-stu-id="52213-109">Remember, these are ADO errors: they result from the ADO operation failing.</span></span> <span data-ttu-id="52213-110">Ошибки, возвращаемые основного поставщика отображаются в виде объектов **ошибок** в семейство **Errors** объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="52213-110">Errors returned by the underlying provider appear as **Error** objects in the **Connection** object's **Errors** collection.</span></span>

<span data-ttu-id="52213-111">\#Директива импорта только создает процедуры обработки ошибок для методов и свойств, объявленных в ADO DLL-файл.</span><span class="sxs-lookup"><span data-stu-id="52213-111">The \#import directive only creates error-handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="52213-112">Тем не менее вы можете воспользоваться преимуществами такой же механизм обработки ошибок, создав собственный проверки ошибок макроса или встроенной функции.</span><span class="sxs-lookup"><span data-stu-id="52213-112">However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</span></span> <span data-ttu-id="52213-113">В разделе расширений Visual C++ для примеров.</span><span class="sxs-lookup"><span data-stu-id="52213-113">See the topic Visual C++ Extensions for examples.</span></span>

