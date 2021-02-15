---
title: Объект DataSpace (RDS)
TOCTitle: DataSpace object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f77617d4ddfb0160b8a418f55582a380067fde70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294465"
---
# <a name="dataspace-object-rds"></a><span data-ttu-id="727b7-102">Объект DataSpace (RDS)</span><span class="sxs-lookup"><span data-stu-id="727b7-102">DataSpace object (RDS)</span></span>

<span data-ttu-id="727b7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="727b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="727b7-104">Создает прокси на стороне клиента для пользовательских бизнес-объектов, расположенных на среднем уровне.</span><span class="sxs-lookup"><span data-stu-id="727b7-104">Creates client-side proxies to custom business objects located on the middle tier.</span></span>

## <a name="remarks"></a><span data-ttu-id="727b7-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="727b7-105">Remarks</span></span>

<span data-ttu-id="727b7-106">Удаленной службе данных необходимы прокси бизнес-объектов, чтобы клиентский компонент могли взаимодействовать с бизнес-объектами, расположенными на среднем уровне.</span><span class="sxs-lookup"><span data-stu-id="727b7-106">Remote Data Service needs business object proxies so that client-side component can communicate with business objects located on the middle tier.</span></span> <span data-ttu-id="727b7-107">Прокси-прокси упрощают упаковку, распаковку и транспортировку (маршалинг) данных [recordset](recordset-object-ado.md) приложения через границы процесса или компьютера.</span><span class="sxs-lookup"><span data-stu-id="727b7-107">Proxies facilitate the packaging, unpackaging, and transport (marshaling) of the application's [Recordset](recordset-object-ado.md) data across process or machine boundaries.</span></span>

<span data-ttu-id="727b7-108">Удаленная служба данных использует **RDS. Метод** [CreateObject](createobject-method-rds.md) объекта DataSpace для создания прокси бизнес-объектов.</span><span class="sxs-lookup"><span data-stu-id="727b7-108">Remote Data Service uses the **RDS.DataSpace** object's [CreateObject](createobject-method-rds.md) method to create business object proxies.</span></span> <span data-ttu-id="727b7-109">Прокси бизнес-объекта динамически создается каждый раз, когда создается экземпляр его аналога бизнес-объекта среднего уровня.</span><span class="sxs-lookup"><span data-stu-id="727b7-109">The business object proxy is dynamically created whenever an instance of its middle-tier business object counterpart is created.</span></span> <span data-ttu-id="727b7-110">Удаленная служба данных поддерживает следующие протоколы: HTTP, HTTPS (HTTP Secure Sockets), DCOM и in-process (клиентские компоненты и бизнес-объект находятся на одном компьютере).</span><span class="sxs-lookup"><span data-stu-id="727b7-110">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP Secure Sockets), DCOM, and in-process (client components and the business object reside on the same computer).</span></span>

> [!NOTE]
> <span data-ttu-id="727b7-111">RDS ведет себя "без состояния" при **RDS. Объект DataSpace** использует протоколы HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="727b7-111">RDS behaves in a "stateless" manner when the **RDS.DataSpace** object uses the HTTP or HTTPS protocols.</span></span> <span data-ttu-id="727b7-112">То есть все внутренние сведения о клиентских запросах удаляются после того, как сервер возвращает ответ.</span><span class="sxs-lookup"><span data-stu-id="727b7-112">That is, any internal information about a client request is discarded after the server returns a response.</span></span>

<span data-ttu-id="727b7-113">Несмотря на то что бизнес-объект существует на протяжении всего времени существования прокси бизнес-объекта, фактически бизнес-объект существует только до тех пор, пока не будет отправлен ответ на запрос.</span><span class="sxs-lookup"><span data-stu-id="727b7-113">Although the business object appears to exist for the lifetime of the business object proxy, the business object actually exists only until a response is sent to a request.</span></span> <span data-ttu-id="727b7-114">Когда выдан запрос (то есть вызывается метод для бизнес-объекта), прокси-сервер открывает новое подключение к серверу и создает новый экземпляр бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="727b7-114">When a request is issued (that is, a method is invoked on the business object), the proxy opens a new connection to the server and the server creates a new instance of the business object.</span></span> <span data-ttu-id="727b7-115">После того как бизнес-объект отвечает на запрос, сервер уничтожает бизнес-объект и закрывает подключение.</span><span class="sxs-lookup"><span data-stu-id="727b7-115">After the business object responds to the request, the server destroys the business object and closes the connection.</span></span>

<span data-ttu-id="727b7-116">Это поведение означает, что нельзя передавать данные из одного запроса в другой с помощью свойства или переменной бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="727b7-116">This behavior means you cannot pass data from one request to another using a business object property or variable.</span></span> <span data-ttu-id="727b7-117">Для сохраняемого состояния необходимо использовать другой механизм, например файл или аргумент метода.</span><span class="sxs-lookup"><span data-stu-id="727b7-117">You must employ some other mechanism, such as a file or a method argument, to persist state data.</span></span>

<span data-ttu-id="727b7-118">ИД класса для **RDS. Объект DataSpace—** BD96C556-65A3-11D0-983A-00C04FC29E36.</span><span class="sxs-lookup"><span data-stu-id="727b7-118">The class ID for the **RDS.DataSpace** object is BD96C556-65A3-11D0-983A-00C04FC29E36.</span></span>

