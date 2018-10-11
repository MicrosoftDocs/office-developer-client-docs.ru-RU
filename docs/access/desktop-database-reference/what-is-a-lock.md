---
title: What is a Lock? (Справочник по для настольных баз данных access)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f852901be41060568bdbad539906e9166d080fad
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481621"
---
# <a name="what-is-a-lock"></a><span data-ttu-id="b205e-103">What is a Lock?</span><span class="sxs-lookup"><span data-stu-id="b205e-103">What is a Lock?</span></span>


<span data-ttu-id="b205e-104">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b205e-104">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b205e-105">Блокировка — это процесс, с помощью которого СУБД ограничивает доступ к строке в многопользовательской среде.</span><span class="sxs-lookup"><span data-stu-id="b205e-105">Locking is the process by which a DBMS restricts access to a row in a multi-user environment.</span></span> <span data-ttu-id="b205e-106">Когда строки или столбца заблокирована, другие пользователи не разрешены для доступа к заблокированной данных до снятия блокировки.</span><span class="sxs-lookup"><span data-stu-id="b205e-106">When a row or column is exclusively locked, other users are not permitted to access the locked data until the lock is released.</span></span> <span data-ttu-id="b205e-107">Это гарантирует, что два пользователя не может одновременно обновить же столбец в строке.</span><span class="sxs-lookup"><span data-stu-id="b205e-107">This ensures that two users cannot simultaneously update the same column in a row.</span></span>

<span data-ttu-id="b205e-108">Блокировки могут быть очень дорогими с точки зрения ресурсов и должен использоваться только в том случае, если требуется, чтобы сохранить целостность данных.</span><span class="sxs-lookup"><span data-stu-id="b205e-108">Locks can be very expensive from a resource perspective and should be used only when required to preserve data integrity.</span></span> <span data-ttu-id="b205e-109">В базе данных, где сотни или тысячи пользователей может попытка получить доступ к записи в секунду — например, базы данных подключения к Интернету — ненужных блокировки быстро может привести к снижению производительности в приложении.</span><span class="sxs-lookup"><span data-stu-id="b205e-109">In a database where hundreds or thousands of users could be trying to access a record every second — such as a database connected to the Internet — unnecessary locking could quickly result in slower performance in your application.</span></span>

<span data-ttu-id="b205e-110">Можно управлять как источник данных и библиотека курсора ADO управление параллелизм, выбрав соответствующий параметр блокировки.</span><span class="sxs-lookup"><span data-stu-id="b205e-110">You can control how the data source and the ADO cursor library manage concurrency by choosing the appropriate locking option.</span></span>

<span data-ttu-id="b205e-111">Присвойте свойству **LockType для** перед открытием **набора записей** , чтобы указать, какой блокировки поставщика следует использовать при открытии его.</span><span class="sxs-lookup"><span data-stu-id="b205e-111">Set the **LockType** property before opening a **Recordset** to specify what type of locking the provider should use when opening it.</span></span> <span data-ttu-id="b205e-112">Чтение свойства для возвращения типа блокировки используется open объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b205e-112">Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="b205e-113">Поставщики могут не поддерживать все типы блокировки.</span><span class="sxs-lookup"><span data-stu-id="b205e-113">Providers might not support all lock types.</span></span> <span data-ttu-id="b205e-114">Если поставщик не поддерживает запрошенный **LockType для** параметра, он будет заменить другой тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="b205e-114">If a provider cannot support the requested **LockType** setting, it will substitute another type of locking.</span></span> <span data-ttu-id="b205e-115">Чтобы определить фактический блокировки функциональные возможности, доступные в объекте **набора записей** , используйте метод [поддерживает](supports-method-ado.md) с **adUpdate** и **adUpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="b205e-115">To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="b205e-116">Параметр **adLockPessimistic** не поддерживается, если свойство [CursorLocation](cursorlocation-property-ado.md) имеет значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="b205e-116">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span> <span data-ttu-id="b205e-117">Если задано значение не поддерживается, сообщение об ошибке не приведет к; ближайший поддерживаемый **LockType для** будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="b205e-117">If an unsupported value is set, no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="b205e-118">Свойство **LockType для** чтения и записи при выполняется **записей** закрытой и только для чтения при открытии.</span><span class="sxs-lookup"><span data-stu-id="b205e-118">The **LockType** property is read/write when the **Recordset** is closed, and read-only when it is open.</span></span>

