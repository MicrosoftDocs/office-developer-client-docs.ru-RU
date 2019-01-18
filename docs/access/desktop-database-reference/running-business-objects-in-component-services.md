---
title: Выполнение бизнес-объектов в службах компонентов
TOCTitle: Running business objects in component services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23cb90161e5e0728aa652ae5d496216676f781a5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719339"
---
# <a name="running-business-objects-in-component-services"></a><span data-ttu-id="9b10d-102">Выполнение бизнес-объектов в службах компонентов</span><span class="sxs-lookup"><span data-stu-id="9b10d-102">Running business objects in component services</span></span>

<span data-ttu-id="9b10d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b10d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b10d-104">Бизнес-объекты могут быть исполняемых файлов (.exe) или библиотеки динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="9b10d-104">Business objects can be executable files (.exe) or dynamic-link libraries (.dll).</span></span> <span data-ttu-id="9b10d-105">Конфигурации, используемые для выполнения бизнес-объекта зависит от объекта .dll или .exe файла:</span><span class="sxs-lookup"><span data-stu-id="9b10d-105">The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</span></span>

- <span data-ttu-id="9b10d-106">Бизнес-объекты, как файлы .exe можно вызвать через DCOM.</span><span class="sxs-lookup"><span data-stu-id="9b10d-106">Business objects created as .exe files can be called through DCOM.</span></span> <span data-ttu-id="9b10d-107">Если эти бизнес-объекты используются через Internet Information Services (IIS), они могут быть marshalingof дополнительные данные, что приводит к снижению производительности клиента.</span><span class="sxs-lookup"><span data-stu-id="9b10d-107">If these business objects are used through Internet Information Services (IIS), they are subject to additional marshalingof data, which will slow client performance.</span></span>

- <span data-ttu-id="9b10d-108">Бизнес-объекты, как DLL-файлы можно использовать с помощью служб IIS (и, следовательно, HTTP).</span><span class="sxs-lookup"><span data-stu-id="9b10d-108">Business objects created as .dll files can be used via IIS (and therefore HTTP).</span></span> <span data-ttu-id="9b10d-109">Они могут также использоваться через DCOM только с помощью службы компонентов (или сервера транзакций, если вы используете Windows NT).</span><span class="sxs-lookup"><span data-stu-id="9b10d-109">They can also be used over DCOM only via Component Services (or Microsoft Transaction Server, if you are using Windows NT).</span></span> <span data-ttu-id="9b10d-110">Бизнес-объект библиотеки DLL, необходимо зарегистрировать на компьютере сервера IIS для предоставления специальных возможностей с помощью служб IIS.</span><span class="sxs-lookup"><span data-stu-id="9b10d-110">Business object DLLs will need to be registered on the IIS server computer to give you accessibility via IIS.</span></span> <span data-ttu-id="9b10d-111">(Для действий по настройке DLL для запуска на DCOM, обратитесь к разделу «[Включение DLL выполнить на DCOM](enabling-a-dll-to-run-on-dcom.md).»)</span><span class="sxs-lookup"><span data-stu-id="9b10d-111">(For steps on how to configure a DLL to run on DCOM, see the section, "[Enabling a DLL to Run on DCOM](enabling-a-dll-to-run-on-dcom.md).")</span></span>


> [!NOTE]
> <span data-ttu-id="9b10d-112">При реализации бизнес-объекты на среднем уровне как компоненты службы компонентов (с помощью **GetObjectContext**, **SetComplete**и **SetAbort**), они могут использовать службы компонентов (или MTS, если вы используете Windows NT) контекст объектов сохранение их состояния между нескольких клиентских вызовов.</span><span class="sxs-lookup"><span data-stu-id="9b10d-112">When business objects on the middle tier are implemented as Component Services components (using **GetObjectContext**, **SetComplete**, and **SetAbort**), they can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</span></span> <span data-ttu-id="9b10d-113">Этот сценарий можно с помощью DCOM, который обычно реализуются между доверенных клиентов и серверов (интрасеть).</span><span class="sxs-lookup"><span data-stu-id="9b10d-113">This scenario is possible with DCOM, which is typically implemented between trusted clients and servers (an intranet).</span></span> 
>
> <span data-ttu-id="9b10d-114">В данном случае [RDS. Пространства данных](dataspace-object-rds.md) объект и метод [CreateObject](createobject-method-rds.md) на стороне клиента, заменяются объект context транзакций и **CreateInstance** метод (интерфейс **ITransactionContext** ), реализованные с помощью службы компонентов.</span><span class="sxs-lookup"><span data-stu-id="9b10d-114">In this case, the [RDS.DataSpace](dataspace-object-rds.md) object and [CreateObject](createobject-method-rds.md) method on the client side are replaced by the transaction context object and **CreateInstance** method (provided by the **ITransactionContext** interface), implemented by Component Services.</span></span>


## <a name="see-also"></a><span data-ttu-id="9b10d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9b10d-115">See also</span></span>

- [<span data-ttu-id="9b10d-116">Выполнение бизнес-объекты в службы компонентов (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="9b10d-116">Running Business Objects in Component Services (SQL Server)</span></span>](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)
