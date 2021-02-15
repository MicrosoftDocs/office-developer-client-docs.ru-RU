---
title: What is a Lock? (Справочник по базам данных Access для настольных ПК)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e503fd15d9864cc6ab007de031493e321622246
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306764"
---
# <a name="what-is-a-lock"></a><span data-ttu-id="b2be3-103">Что такое блокировка?</span><span class="sxs-lookup"><span data-stu-id="b2be3-103">What is a lock?</span></span>


<span data-ttu-id="b2be3-104">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2be3-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2be3-105">Блокировка — это процесс, с помощью которого DBMS ограничивает доступ к строке в среде с несколькими пользователями.</span><span class="sxs-lookup"><span data-stu-id="b2be3-105">Locking is the process by which a DBMS restricts access to a row in a multi-user environment.</span></span> <span data-ttu-id="b2be3-106">Если строка или столбец заблокированы исключительно, другим пользователям не разрешается доступ к заблокированным данным, пока блокировка не будет отпущена.</span><span class="sxs-lookup"><span data-stu-id="b2be3-106">When a row or column is exclusively locked, other users are not permitted to access the locked data until the lock is released.</span></span> <span data-ttu-id="b2be3-107">Это гарантирует, что два пользователя не смогут одновременно обновлять один и тот же столбец в строке.</span><span class="sxs-lookup"><span data-stu-id="b2be3-107">This ensures that two users cannot simultaneously update the same column in a row.</span></span>

<span data-ttu-id="b2be3-108">Блокировки могут быть очень дорогими с точки зрения ресурсов и должны использоваться только в том случае, если это необходимо для сохранения целостности данных.</span><span class="sxs-lookup"><span data-stu-id="b2be3-108">Locks can be very expensive from a resource perspective and should be used only when required to preserve data integrity.</span></span> <span data-ttu-id="b2be3-109">В базе данных, где сотни или тысячи пользователей могут пытаться получить доступ к записи каждую секунду ( например, к базе данных, подключенной к Интернету), ненужные блокировки могут быстро привести к замедлению производительности приложения.</span><span class="sxs-lookup"><span data-stu-id="b2be3-109">In a database where hundreds or thousands of users could be trying to access a record every second — such as a database connected to the Internet — unnecessary locking could quickly result in slower performance in your application.</span></span>

<span data-ttu-id="b2be3-110">Вы можете управлять тем, как источник данных и библиотека курсоров ADO управляются, выбрав соответствующий параметр блокировки.</span><span class="sxs-lookup"><span data-stu-id="b2be3-110">You can control how the data source and the ADO cursor library manage concurrency by choosing the appropriate locking option.</span></span>

<span data-ttu-id="b2be3-111">Закажите **свойство LockType** перед открытием **набора записей,** чтобы указать, какой тип блокировки должен использовать поставщик при его открытии.</span><span class="sxs-lookup"><span data-stu-id="b2be3-111">Set the **LockType** property before opening a **Recordset** to specify what type of locking the provider should use when opening it.</span></span> <span data-ttu-id="b2be3-112">Прочитайте свойство, чтобы вернуть тип блокировки, используемой для открытого **объекта Recordset.**</span><span class="sxs-lookup"><span data-stu-id="b2be3-112">Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="b2be3-113">Поставщики могут поддерживать не все типы блокировки.</span><span class="sxs-lookup"><span data-stu-id="b2be3-113">Providers might not support all lock types.</span></span> <span data-ttu-id="b2be3-114">Если поставщик не может поддерживать запрашиваемую настройку **LockType,** он заменит другой тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="b2be3-114">If a provider cannot support the requested **LockType** setting, it will substitute another type of locking.</span></span> <span data-ttu-id="b2be3-115">Чтобы определить фактические функции блокировки, доступные в объекте **Recordset,** используйте метод [Supports](supports-method-ado.md) с **adUpdate** и **adUpdateBatch.**</span><span class="sxs-lookup"><span data-stu-id="b2be3-115">To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="b2be3-116">Параметр **adLockPessimistic** не поддерживается, если свойство [CursorLocation](cursorlocation-property-ado.md) имеет свойство **adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="b2be3-116">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span> <span data-ttu-id="b2be3-117">Если установлено неподтверченные значения, ошибка не будет; Будет использоваться **ближайший поддерживаемый LockType.**</span><span class="sxs-lookup"><span data-stu-id="b2be3-117">If an unsupported value is set, no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="b2be3-118">Свойство **LockType** считывать и записывать при закрытии **объекта Recordset** и только для чтения при его открытом режиме.</span><span class="sxs-lookup"><span data-stu-id="b2be3-118">The **LockType** property is read/write when the **Recordset** is closed, and read-only when it is open.</span></span>

<span data-ttu-id="b2be3-119">В этом разделе содержится следующий раздел:</span><span class="sxs-lookup"><span data-stu-id="b2be3-119">This section includes the following topic:</span></span>

- [<span data-ttu-id="b2be3-120">Types of Locks</span><span class="sxs-lookup"><span data-stu-id="b2be3-120">Types of Locks</span></span>](types-of-locks.md)

