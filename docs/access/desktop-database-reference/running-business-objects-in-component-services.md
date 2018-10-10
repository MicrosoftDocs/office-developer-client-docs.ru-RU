---
title: Running Business Objects in Component Services
TOCTitle: Running Business Objects in Component Services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41424fd62e915ecb2d54fdb49c939b788f458804
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480979"
---
# <a name="running-business-objects-in-component-services"></a><span data-ttu-id="5dfd7-102">Running Business Objects in Component Services</span><span class="sxs-lookup"><span data-stu-id="5dfd7-102">Running Business Objects in Component Services</span></span>


<span data-ttu-id="5dfd7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5dfd7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5dfd7-104">Бизнес-объекты могут быть исполняемых файлов (.exe) или библиотеки динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="5dfd7-104">Business objects can be executable files (.exe) or dynamic-link libraries (.dll).</span></span> <span data-ttu-id="5dfd7-105">Конфигурации, используемые для выполнения бизнес-объекта зависит от объекта .dll или .exe файла:</span><span class="sxs-lookup"><span data-stu-id="5dfd7-105">The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</span></span>

  - <span data-ttu-id="5dfd7-106">Бизнес-объекты, как файлы .exe можно вызвать через DCOM.</span><span class="sxs-lookup"><span data-stu-id="5dfd7-106">Business objects created as .exe files can be called through DCOM.</span></span> <span data-ttu-id="5dfd7-107">Если эти бизнес-объекты используются через Internet Information Services (IIS), они могут быть marshalingof дополнительные данные, что приводит к снижению производительности клиента.</span><span class="sxs-lookup"><span data-stu-id="5dfd7-107">If these business objects are used through Internet Information Services (IIS), they are subject to additional marshalingof data, which will slow client performance.</span></span>

  - <span data-ttu-id="5dfd7-108">Бизнес-объекты, как DLL-файлы можно использовать с помощью служб IIS (и, следовательно, HTTP).</span><span class="sxs-lookup"><span data-stu-id="5dfd7-108">Business objects created as .dll files can be used via IIS (and therefore HTTP).</span></span> <span data-ttu-id="5dfd7-109">Они могут также использоваться через DCOM только с помощью службы компонентов (или сервера транзакций, если вы используете Windows NT).</span><span class="sxs-lookup"><span data-stu-id="5dfd7-109">They can also be used over DCOM only via Component Services (or Microsoft Transaction Server, if you are using Windows NT).</span></span> <span data-ttu-id="5dfd7-110">Бизнес-объект библиотеки DLL, необходимо зарегистрировать на компьютере сервера IIS для предоставления специальных возможностей с помощью служб IIS.</span><span class="sxs-lookup"><span data-stu-id="5dfd7-110">Business object DLLs will need to be registered on the IIS server computer to give you accessibility via IIS.</span></span> <span data-ttu-id="5dfd7-111">(Для действий по настройке DLL для запуска на DCOM, обратитесь к разделу «[Включение DLL выполнить на DCOM](enabling-a-dll-to-run-on-dcom.md).»)</span><span class="sxs-lookup"><span data-stu-id="5dfd7-111">(For steps on how to configure a DLL to run on DCOM, see the section, "[Enabling a DLL to Run on DCOM](enabling-a-dll-to-run-on-dcom.md).")</span></span>


> [!NOTE]
> <P><span data-ttu-id="5dfd7-112">При реализации бизнес-объекты на среднем уровне как компоненты службы компонентов (с помощью <STRONG>GetObjectContext</STRONG>, <STRONG>SetComplete</STRONG>и <STRONG>SetAbort</STRONG>), они могут использовать службы компонентов (или MTS, если вы используете Windows NT) контекст объектов сохранение их состояния между нескольких клиентских вызовов.</span><span class="sxs-lookup"><span data-stu-id="5dfd7-112">When business objects on the middle tier are implemented as Component Services components (using <STRONG>GetObjectContext</STRONG>, <STRONG>SetComplete</STRONG>, and <STRONG>SetAbort</STRONG>), they can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</span></span> <span data-ttu-id="5dfd7-113">Этот сценарий можно с помощью DCOM, который обычно реализуются между доверенных клиентов и серверов (интрасеть).</span><span class="sxs-lookup"><span data-stu-id="5dfd7-113">This scenario is possible with DCOM, which is typically implemented between trusted clients and servers (an intranet).</span></span> <span data-ttu-id="5dfd7-114">В данном случае <A href="dataspace-object-rds.md">RDS. Пространства данных</A> объект и метод <A href="createobject-method-rds.md">CreateObject</A> на стороне клиента, заменяются объект context транзакций и <STRONG>CreateInstance</STRONG> метод (интерфейс <STRONG>ITransactionContext</STRONG> ), реализованные с помощью службы компонентов.</span><span class="sxs-lookup"><span data-stu-id="5dfd7-114">In this case, the <A href="dataspace-object-rds.md">RDS.DataSpace</A> object and <A href="createobject-method-rds.md">CreateObject</A> method on the client side are replaced by the transaction context object and <STRONG>CreateInstance</STRONG> method (provided by the <STRONG>ITransactionContext</STRONG> interface), implemented by Component Services.</span></span></P>


