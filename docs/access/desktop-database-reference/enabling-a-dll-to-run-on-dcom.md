---
title: Подготовка библиотеки DLL к работе в DCOM
TOCTitle: Enabling a DLL to run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b97f4e8050cf293621c7b7fc79437c89171d86fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293548"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a><span data-ttu-id="f5df5-102">Подготовка библиотеки DLL к работе в DCOM</span><span class="sxs-lookup"><span data-stu-id="f5df5-102">Enabling a DLL to run on DCOM</span></span>


<span data-ttu-id="f5df5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5df5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5df5-104">Ниже описано, как включить библиотеки динамической связи бизнес-объектов для использования DCOM и Microsoft IIS (HTTP) через службы компонентов.</span><span class="sxs-lookup"><span data-stu-id="f5df5-104">The following steps outline how to enable a business object dynamic-link libraries to use both DCOM and Microsoft Internet Information Services (HTTP) via Component Services.</span></span>

1.  <span data-ttu-id="f5df5-105">Создайте пустой пакет в оснастке MMC "Службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="f5df5-105">Create a new empty package in the Component Services MMC snap-in.</span></span> <span data-ttu-id="f5df5-106">Для создания пакета и добавления DLL в этот пакет используется оснастка MMC "Службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="f5df5-106">You will use the Component Services MMC snap-in to create a package and add the DLL into this package.</span></span> <span data-ttu-id="f5df5-107">Это делает DLL-DLL доступным через DCOM, но удаляет их с помощью IIS.</span><span class="sxs-lookup"><span data-stu-id="f5df5-107">This makes the .dll accessible through DCOM, but it removes the accessibility through IIS.</span></span> <span data-ttu-id="f5df5-108">(Если вы зарегиструете реестр для DLL, ключ **Inproc** будет пустым. При установке атрибута Активация, как поясняется далее в этом разделе, добавляется значение в ключ **Inproc.)**</span><span class="sxs-lookup"><span data-stu-id="f5df5-108">(If you check in the registry for the .dll, the **Inproc** key is now empty; setting the Activation attribute, explained later in this topic, adds a value in the **Inproc** key.)</span></span>

2.  <span data-ttu-id="f5df5-109">Установите в пакет бизнес-объект.</span><span class="sxs-lookup"><span data-stu-id="f5df5-109">Install a business object into the package.</span></span> <span data-ttu-id="f5df5-110">-or- Импортировать [объект RDSServer.DataFactory](datafactory-object-rdsserver.md) в пакет.</span><span class="sxs-lookup"><span data-stu-id="f5df5-110">-or- Import the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object into the package.</span></span>

3.  <span data-ttu-id="f5df5-111">Установите для атрибута Activation для пакета параметр **In the creator's process** (Library application).</span><span class="sxs-lookup"><span data-stu-id="f5df5-111">Set the Activation attribute for the package to **In the creator's process** (Library application).</span></span> <span data-ttu-id="f5df5-112">Чтобы сделать DLL-DLL доступным через DCOM и IIS на одном компьютере, необходимо установить атрибут активации компонента в оснастке MMC "Службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="f5df5-112">To make the .dll accessible through DCOM and IIS on the same computer, you must set the component's Activation attribute in the Component Services MMC snap-in.</span></span> <span data-ttu-id="f5df5-113">После того как вы установите для атрибута значение In **the creator's process,** вы заметите, что в реестр добавлен ключ **inproc-сервера,** который указывает на заменяющие DLL службы компонентов.</span><span class="sxs-lookup"><span data-stu-id="f5df5-113">After you set the attribute to **In the creator's process**, you will notice that an **Inproc** server key in the registry has been added that points to a Component Services surrogate .dll.</span></span>

