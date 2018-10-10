---
title: Anticipating Errors
TOCTitle: Anticipating Errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f062eb86b45778cc7f25fb2d0d0588b82bdd78b3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482381"
---
# <a name="anticipating-errors"></a><span data-ttu-id="c6028-102">Anticipating Errors</span><span class="sxs-lookup"><span data-stu-id="c6028-102">Anticipating Errors</span></span>


<span data-ttu-id="c6028-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6028-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c6028-104">Предотвращение ошибок по крайней мере важно, как обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="c6028-104">Error prevention is at least as important as error handling.</span></span> <span data-ttu-id="c6028-105">В этом последнем разделе со списком short меры предосторожности, которые приложение может воспользоваться для ошибки, скорее всего, будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="c6028-105">This final section contains a short list of precautions your application can take to help make errors less likely to occur.</span></span>

<span data-ttu-id="c6028-106">Проверьте состояние объектов, проверив значение свойства **состояние** перед попыткой выполнения операции с помощью этих объектов.</span><span class="sxs-lookup"><span data-stu-id="c6028-106">Check the state of objects by checking the value in the **State** property before trying to perform an operation using those objects.</span></span> <span data-ttu-id="c6028-107">Например если приложение использует глобальные **подключения**, проверьте значение свойства **состояние** является ли уже открыт до вызова метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="c6028-107">For example, if your application uses a global **Connection**, check its **State** property to see if it is already open before calling the **Open** method.</span></span>

  - <span data-ttu-id="c6028-108">Все программы, которые принимает данные от пользователя необходимо включить код для проверки данных перед отправкой в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="c6028-108">Any program that accepts data from a user must include code to validate that data before sending it to the data store.</span></span> <span data-ttu-id="c6028-109">Нельзя полагаться на хранилище данных, поставщик, ADO или даже язык программирования сообщать о неполадках.</span><span class="sxs-lookup"><span data-stu-id="c6028-109">You cannot rely on the data store, the provider, ADO, or even your programming language to notify you of problems.</span></span> <span data-ttu-id="c6028-110">Необходимо проверить каждый байт, введенных пользователями, убедившись, что данные правильный ее тип поля и обязательные поля не являются пустыми.</span><span class="sxs-lookup"><span data-stu-id="c6028-110">You must check every byte entered by your users, making sure that data is the correct type for its field and that required fields are not empty.</span></span>

<span data-ttu-id="c6028-111">Проверьте данные, прежде чем записи данных в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="c6028-111">Check the data before you try to write any data to the data store.</span></span> <span data-ttu-id="c6028-112">Для этого проще всего обрабатывать события **WillMove** или **WillUpdateRecordset** события.</span><span class="sxs-lookup"><span data-stu-id="c6028-112">The easiest way to do so is to handle the **WillMove** event or the **WillUpdateRecordset** event.</span></span> <span data-ttu-id="c6028-113">Более подробные сведения об обработке событий ADO, в разделе [Глава 7: обработка событий ADO](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="c6028-113">For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

<span data-ttu-id="c6028-114">Убедитесь в том, что **набора записей** объекты не за пределами **записей** перед попыткой перемещения указателя записи.</span><span class="sxs-lookup"><span data-stu-id="c6028-114">Make sure that **Recordset** objects are not beyond the boundaries of the **Recordset** before attempting to move the record pointer.</span></span> <span data-ttu-id="c6028-115">При попытке **MoveNext** Если **EOF** имеет значение True или **MovePrev** , если **BOF** имеет значение True, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="c6028-115">If you try to **MoveNext** when **EOF** is True or **MovePrev** when **BOF** is True, an error will occur.</span></span> <span data-ttu-id="c6028-116">При выполнении любой из методов **перемещения** , когда **EOF** и **BOF** имеют значение True, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="c6028-116">If you perform any of the **Move** methods when both **EOF** and **BOF** are True, an error will be generated.</span></span>

<span data-ttu-id="c6028-117">Также возникают ошибки при попытке выполнения операции, такие как \*\*файлы и **поиска** \*\* на пустой **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="c6028-117">Errors also will occur if you try to perform operations such as **Seek** and **Find** on an empty **Recordset**.</span></span>

