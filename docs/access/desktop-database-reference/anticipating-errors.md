---
title: Предугадывание ошибок
TOCTitle: Anticipating errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4bd130ca05527c7761ca587781c1fd4f939ebe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297174"
---
# <a name="anticipating-errors"></a><span data-ttu-id="39fb3-102">Предугадывание ошибок</span><span class="sxs-lookup"><span data-stu-id="39fb3-102">Anticipating errors</span></span>


<span data-ttu-id="39fb3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39fb3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39fb3-104">Предотвращение ошибок по крайней мере так же важно, как и обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="39fb3-104">Error prevention is at least as important as error handling.</span></span> <span data-ttu-id="39fb3-105">В этом заключительном разделе содержится краткий список мер предосторожности, которые может принять ваше приложение, чтобы уменьшить вероятность возникновения ошибок.</span><span class="sxs-lookup"><span data-stu-id="39fb3-105">This final section contains a short list of precautions your application can take to help make errors less likely to occur.</span></span>

<span data-ttu-id="39fb3-106">Проверьте состояние объектов, проверив значение в свойстве **State,** прежде чем пытаться выполнить операцию с использованием этих объектов.</span><span class="sxs-lookup"><span data-stu-id="39fb3-106">Check the state of objects by checking the value in the **State** property before trying to perform an operation using those objects.</span></span> <span data-ttu-id="39fb3-107">Например, если приложение использует глобальное **подключение,** проверьте его свойство **State,** чтобы проверить, открыто ли оно, прежде чем вызывать **метод Open.**</span><span class="sxs-lookup"><span data-stu-id="39fb3-107">For example, if your application uses a global **Connection**, check its **State** property to see if it is already open before calling the **Open** method.</span></span>

- <span data-ttu-id="39fb3-108">Любая программа, которая принимает данные от пользователя, должна включать код для проверки этих данных перед их отправкой в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="39fb3-108">Any program that accepts data from a user must include code to validate that data before sending it to the data store.</span></span> <span data-ttu-id="39fb3-109">Для уведомления о проблемах нельзя полагаться на хранилище данных, поставщика, ADO или даже язык программирования.</span><span class="sxs-lookup"><span data-stu-id="39fb3-109">You cannot rely on the data store, the provider, ADO, or even your programming language to notify you of problems.</span></span> <span data-ttu-id="39fb3-110">Необходимо проверить каждый введенный пользователем тип данных, чтобы убедиться, что данные являются правильным типом для поля и что необходимые поля не пусты.</span><span class="sxs-lookup"><span data-stu-id="39fb3-110">You must check every byte entered by your users, making sure that data is the correct type for its field and that required fields are not empty.</span></span>

<span data-ttu-id="39fb3-111">Проверьте данные, прежде чем пытаться записать какие-либо данные в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="39fb3-111">Check the data before you try to write any data to the data store.</span></span> <span data-ttu-id="39fb3-112">Самый простой способ сделать это — обработать событие **WillMove** или **WillUpdateRecordset.**</span><span class="sxs-lookup"><span data-stu-id="39fb3-112">The easiest way to do so is to handle the **WillMove** event or the **WillUpdateRecordset** event.</span></span> <span data-ttu-id="39fb3-113">Более подробное обсуждение обработки событий ADO см. в главе [7 "Обработка событий ADO".](chapter-7-handling-ado-events.md)</span><span class="sxs-lookup"><span data-stu-id="39fb3-113">For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

<span data-ttu-id="39fb3-114">Перед попыткой переместить указатель записи убедитесь, что объекты **Recordset** не выходят за пределы объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="39fb3-114">Make sure that **Recordset** objects are not beyond the boundaries of the **Recordset** before attempting to move the record pointer.</span></span> <span data-ttu-id="39fb3-115">При попытке **moveNext,** если **EOF** имеет true или **MovePrev,** когда **BOF** имеет true, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="39fb3-115">If you try to **MoveNext** when **EOF** is True or **MovePrev** when **BOF** is True, an error will occur.</span></span> <span data-ttu-id="39fb3-116">Если вы выполняете какой-либо из методов **Move,** если **и EOF,** и **BOF** имеют true, будет выдана ошибка.</span><span class="sxs-lookup"><span data-stu-id="39fb3-116">If you perform any of the **Move** methods when both **EOF** and **BOF** are True, an error will be generated.</span></span>

<span data-ttu-id="39fb3-117">Ошибки также возникают при попытке выполнения таких операций, как **Seek** и **Find** на пустом **наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="39fb3-117">Errors also will occur if you try to perform operations such as **Seek** and **Find** on an empty **Recordset**.</span></span>

