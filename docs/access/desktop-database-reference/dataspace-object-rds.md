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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716568"
---
# <a name="dataspace-object-rds"></a><span data-ttu-id="592fb-102">Объект DataSpace (RDS)</span><span class="sxs-lookup"><span data-stu-id="592fb-102">DataSpace object (RDS)</span></span>

<span data-ttu-id="592fb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="592fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="592fb-104">Создает прокси-серверы со стороны клиента и настраиваемых бизнес-объектов, расположенной на среднем уровне.</span><span class="sxs-lookup"><span data-stu-id="592fb-104">Creates client-side proxies to custom business objects located on the middle tier.</span></span>

## <a name="remarks"></a><span data-ttu-id="592fb-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="592fb-105">Remarks</span></span>

<span data-ttu-id="592fb-106">Удаленной службы данных должна business объекта прокси-серверы, соответствующего компонента со стороны клиента может устанавливать связь с бизнес-объекты, расположенные на среднем уровне.</span><span class="sxs-lookup"><span data-stu-id="592fb-106">Remote Data Service needs business object proxies so that client-side component can communicate with business objects located on the middle tier.</span></span> <span data-ttu-id="592fb-107">Прокси-серверы упрощают создание пакета, содержащего, распаковке и транспорта (маршалинга) приложения [записей](recordset-object-ado.md) данных через границы процесса или компьютера.</span><span class="sxs-lookup"><span data-stu-id="592fb-107">Proxies facilitate the packaging, unpackaging, and transport (marshaling) of the application's [Recordset](recordset-object-ado.md) data across process or machine boundaries.</span></span>

<span data-ttu-id="592fb-108">Служба удаленного данных использует **RDS. Пространства данных** метод [CreateObject](createobject-method-rds.md) объекта для создания объекта business прокси-серверы.</span><span class="sxs-lookup"><span data-stu-id="592fb-108">Remote Data Service uses the **RDS.DataSpace** object's [CreateObject](createobject-method-rds.md) method to create business object proxies.</span></span> <span data-ttu-id="592fb-109">Прокси-сервера business object динамически создается при создании экземпляра от своего аналога среднего уровня бизнес-объектов.</span><span class="sxs-lookup"><span data-stu-id="592fb-109">The business object proxy is dynamically created whenever an instance of its middle-tier business object counterpart is created.</span></span> <span data-ttu-id="592fb-110">Служба удаленных данных поддерживает следующие протоколы: HTTP, HTTPS (Secure HTTP Sockets), DCOM и внутрипроцессный (клиентские компоненты и бизнес-объекты хранятся на том же компьютере).</span><span class="sxs-lookup"><span data-stu-id="592fb-110">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP Secure Sockets), DCOM, and in-process (client components and the business object reside on the same computer).</span></span>

> [!NOTE]
> <span data-ttu-id="592fb-111">Ведет себя служб удаленных рабочих СТОЛОВ в виде «без сведений о состоянии» при **RDS. Пространства данных** объект использует протоколов HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="592fb-111">RDS behaves in a "stateless" manner when the **RDS.DataSpace** object uses the HTTP or HTTPS protocols.</span></span> <span data-ttu-id="592fb-112">То есть все внутренние сведения о запрос клиента удаляется после сервер возвращает ответ.</span><span class="sxs-lookup"><span data-stu-id="592fb-112">That is, any internal information about a client request is discarded after the server returns a response.</span></span>

<span data-ttu-id="592fb-113">Хотя существует в течение времени жизни прокси-сервера business object бизнес-объект, бизнес-объект действительно существует только в том случае, пока ответ на запрос.</span><span class="sxs-lookup"><span data-stu-id="592fb-113">Although the business object appears to exist for the lifetime of the business object proxy, the business object actually exists only until a response is sent to a request.</span></span> <span data-ttu-id="592fb-114">Если выдается запрос (то есть, вызывается метод на бизнес-объект), прокси-сервер открывается новое подключение к серверу и сервер создает новый экземпляр объекта бизнеса.</span><span class="sxs-lookup"><span data-stu-id="592fb-114">When a request is issued (that is, a method is invoked on the business object), the proxy opens a new connection to the server and the server creates a new instance of the business object.</span></span> <span data-ttu-id="592fb-115">После бизнес-объект отвечает на запрос, сервер уничтожает бизнес-объекта и закрывает подключение.</span><span class="sxs-lookup"><span data-stu-id="592fb-115">After the business object responds to the request, the server destroys the business object and closes the connection.</span></span>

<span data-ttu-id="592fb-116">Это означает, что нельзя передачи данных от одного запроса на другую с помощью переменной или свойству объекта business.</span><span class="sxs-lookup"><span data-stu-id="592fb-116">This behavior means you cannot pass data from one request to another using a business object property or variable.</span></span> <span data-ttu-id="592fb-117">Необходимо использовать другой механизм, например файла или аргумента метода, чтобы сохранить данные состояния.</span><span class="sxs-lookup"><span data-stu-id="592fb-117">You must employ some other mechanism, such as a file or a method argument, to persist state data.</span></span>

<span data-ttu-id="592fb-118">КОД класса для **RDS. Пространства данных** объект является BD96C556-65A3 - 11D 0-983A-00C04FC29E36.</span><span class="sxs-lookup"><span data-stu-id="592fb-118">The class ID for the **RDS.DataSpace** object is BD96C556-65A3-11D0-983A-00C04FC29E36.</span></span>

