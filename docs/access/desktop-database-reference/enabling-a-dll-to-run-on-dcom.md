---
title: Включение библиотеки DLL для запуска на DCOM
TOCTitle: Enabling a DLL to run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9feb189221a1d447e6c2e0242240ca13784b7fe
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946463"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a><span data-ttu-id="979fa-102">Включение библиотеки DLL для запуска на DCOM</span><span class="sxs-lookup"><span data-stu-id="979fa-102">Enabling a DLL to run on DCOM</span></span>


<span data-ttu-id="979fa-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="979fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="979fa-104">Следующие шаги показывают, как включить динамические библиотеки объектов business использование DCOM и Microsoft Internet сведения служб (HTTP) с помощью службы компонентов.</span><span class="sxs-lookup"><span data-stu-id="979fa-104">The following steps outline how to enable a business object dynamic-link libraries to use both DCOM and Microsoft Internet Information Services (HTTP) via Component Services.</span></span>

1.  <span data-ttu-id="979fa-105">Создайте новый пустой пакет в оснастке служб консоли Управления компонента.</span><span class="sxs-lookup"><span data-stu-id="979fa-105">Create a new empty package in the Component Services MMC snap-in.</span></span> <span data-ttu-id="979fa-106">Компонент служб MMC-оснастку будет использоваться для создания пакета и добавления библиотеки DLL в этот пакет.</span><span class="sxs-lookup"><span data-stu-id="979fa-106">You will use the Component Services MMC snap-in to create a package and add the DLL into this package.</span></span> <span data-ttu-id="979fa-107">Это делает библиотеки DLL через DCOM, но удаляет специальными возможностями IIS.</span><span class="sxs-lookup"><span data-stu-id="979fa-107">This makes the .dll accessible through DCOM, but it removes the accessibility through IIS.</span></span> <span data-ttu-id="979fa-108">(Если установить в реестре для библиотеки DLL **Inproc** ключ пустая; Установка атрибута активации, описано далее в этом разделе, добавляет значение раздела **Inproc** .)</span><span class="sxs-lookup"><span data-stu-id="979fa-108">(If you check in the registry for the .dll, the **Inproc** key is now empty; setting the Activation attribute, explained later in this topic, adds a value in the **Inproc** key.)</span></span>

2.  <span data-ttu-id="979fa-109">Установка бизнес-объект в пакет.</span><span class="sxs-lookup"><span data-stu-id="979fa-109">Install a business object into the package.</span></span> <span data-ttu-id="979fa-110">- или - импорт [RDSServer.DataFactory](datafactory-object-rdsserver.md) объектов в пакете.</span><span class="sxs-lookup"><span data-stu-id="979fa-110">-or- Import the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object into the package.</span></span>

3.  <span data-ttu-id="979fa-111">Присвойте атрибуту активации для пакета **в процессе создателя** (библиотека приложение).</span><span class="sxs-lookup"><span data-stu-id="979fa-111">Set the Activation attribute for the package to **In the creator's process** (Library application).</span></span> <span data-ttu-id="979fa-112">Чтобы библиотеки DLL доступен через DCOM и службы IIS на том же компьютере, необходимо задать атрибут активации компонента в оснастке служб консоли Управления компонент.</span><span class="sxs-lookup"><span data-stu-id="979fa-112">To make the .dll accessible through DCOM and IIS on the same computer, you must set the component's Activation attribute in the Component Services MMC snap-in.</span></span> <span data-ttu-id="979fa-113">После установки атрибута **в процессе создателя**, можно заметить, что был добавлен ключа сервера **Inproc** реестра, что указывает на службы компонентов заменяемых .dll.</span><span class="sxs-lookup"><span data-stu-id="979fa-113">After you set the attribute to **In the creator's process**, you will notice that an **Inproc** server key in the registry has been added that points to a Component Services surrogate .dll.</span></span>

