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
# <a name="anticipating-errors"></a><span data-ttu-id="dc50d-102">Предугадывание ошибок</span><span class="sxs-lookup"><span data-stu-id="dc50d-102">Anticipating errors</span></span>


<span data-ttu-id="dc50d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc50d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc50d-104">Предотвращение ошибок не менее важно, чем обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="dc50d-104">Error prevention is at least as important as error handling.</span></span> <span data-ttu-id="dc50d-105">В этом последнем разделе содержится краткий список предосторожностей, которые может предпринять приложение, чтобы упростить снижение вероятности возникновения ошибок.</span><span class="sxs-lookup"><span data-stu-id="dc50d-105">This final section contains a short list of precautions your application can take to help make errors less likely to occur.</span></span>

<span data-ttu-id="dc50d-106">Проверьте состояние объектов, проверив значение в свойстве **State** перед попыткой выполнить операцию, используя эти объекты.</span><span class="sxs-lookup"><span data-stu-id="dc50d-106">Check the state of objects by checking the value in the **State** property before trying to perform an operation using those objects.</span></span> <span data-ttu-id="dc50d-107">Например, если приложение использует глобальное **Подключение**, проверьте его свойство **State** , чтобы убедиться, что он уже открыт перед вызовом метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="dc50d-107">For example, if your application uses a global **Connection**, check its **State** property to see if it is already open before calling the **Open** method.</span></span>

- <span data-ttu-id="dc50d-108">Любая программа, принимающая данные от пользователя, должна содержать код для проверки их перед отправкой в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="dc50d-108">Any program that accepts data from a user must include code to validate that data before sending it to the data store.</span></span> <span data-ttu-id="dc50d-109">Вы не можете использовать хранилище данных, поставщик, ADO или даже язык программирования для уведомления о проблемах.</span><span class="sxs-lookup"><span data-stu-id="dc50d-109">You cannot rely on the data store, the provider, ADO, or even your programming language to notify you of problems.</span></span> <span data-ttu-id="dc50d-110">Необходимо проверить все байты, введенные пользователями, убедившись, что данные имеют правильный тип для поля и что обязательные поля не пусты.</span><span class="sxs-lookup"><span data-stu-id="dc50d-110">You must check every byte entered by your users, making sure that data is the correct type for its field and that required fields are not empty.</span></span>

<span data-ttu-id="dc50d-111">Проверьте данные перед попыткой записи данных в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="dc50d-111">Check the data before you try to write any data to the data store.</span></span> <span data-ttu-id="dc50d-112">Самый простой способ сделать это — обработать событие **события WillMove** или событие **виллупдатерекордсет** .</span><span class="sxs-lookup"><span data-stu-id="dc50d-112">The easiest way to do so is to handle the **WillMove** event or the **WillUpdateRecordset** event.</span></span> <span data-ttu-id="dc50d-113">Более подробное описание обработки событий ADO приведено в [главе 7: обработка событий ADO](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="dc50d-113">For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

<span data-ttu-id="dc50d-114">Прежде чем пытаться переместить указатель записи, убедитесь, что объекты **Recordset** выходят за границы **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="dc50d-114">Make sure that **Recordset** objects are not beyond the boundaries of the **Recordset** before attempting to move the record pointer.</span></span> <span data-ttu-id="dc50d-115">Если вы попробуете **MoveNext** , когда **EOF** имеет значение true или **Мовепрев** , когда **BOF** имеет значение true, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="dc50d-115">If you try to **MoveNext** when **EOF** is True or **MovePrev** when **BOF** is True, an error will occur.</span></span> <span data-ttu-id="dc50d-116">Если вы выполняете любой из методов **Move** , когда **EOF EOF** и **BOF** имеет значение true, будет создано сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="dc50d-116">If you perform any of the **Move** methods when both **EOF** and **BOF** are True, an error will be generated.</span></span>

<span data-ttu-id="dc50d-117">Кроме того, при попытке выполнить такие операции **, как поиск** и **Поиск** в пустом объекте **Recordset**, будут возникать ошибки.</span><span class="sxs-lookup"><span data-stu-id="dc50d-117">Errors also will occur if you try to perform operations such as **Seek** and **Find** on an empty **Recordset**.</span></span>

