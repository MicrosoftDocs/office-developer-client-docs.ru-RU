---
title: Пометка бизнес-объектов как безопасных для написания скриптов
TOCTitle: Marking business objects as safe for scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe5d331b7f3ab4685cb930323076d111a25ec68e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289779"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a><span data-ttu-id="931ba-102">Пометка бизнес-объектов как безопасных для написания скриптов</span><span class="sxs-lookup"><span data-stu-id="931ba-102">Marking business objects as safe for scripting</span></span>

<span data-ttu-id="931ba-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="931ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="931ba-104">Чтобы обеспечить безопасную интернет-среду, необходимо отметить любые бизнес-объекты, мгновенные с [помощью RDS. Метод CreateObject](dataspace-object-rds.md) объекта [DataSpace](createobject-method-rds.md) как "безопасный для сценариев".</span><span class="sxs-lookup"><span data-stu-id="931ba-104">To help ensure a secure Internet environment, you need to mark any business objects instantiated with the [RDS.DataSpace](dataspace-object-rds.md) object's [CreateObject](createobject-method-rds.md) method as "safe for scripting."</span></span> <span data-ttu-id="931ba-105">Необходимо убедиться, что они помечены как таковой в области лицензий системного реестра, прежде чем их можно будет использовать в DCOM.</span><span class="sxs-lookup"><span data-stu-id="931ba-105">You need to ensure they are marked as such in the License area of the system registry before they can be used in DCOM.</span></span>

<span data-ttu-id="931ba-106">Чтобы вручную пометить бизнес-объект как безопасный для скриптов, создайте текстовый файл с расширением .reg, содержат следующий текст.</span><span class="sxs-lookup"><span data-stu-id="931ba-106">To manually mark your business object as safe for scripting, create a text file with a .reg extension that contains the following text.</span></span> <span data-ttu-id="931ba-107">Следующие два номера позволяют включить функцию безопасного сценария:</span><span class="sxs-lookup"><span data-stu-id="931ba-107">The following two numbers enable the safe-for-scripting feature:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

<span data-ttu-id="931ba-108">где \< *MyActiveXGUID* \> — это hexadecimal GUID-номер бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="931ba-108">where \<*MyActiveXGUID*\> is the hexadecimal GUID number of your business object.</span></span> <span data-ttu-id="931ba-109">Сохраните его и объедините в реестр с помощью редактора реестра или дважды щелкнув файл .reg в Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="931ba-109">Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</span></span>

<span data-ttu-id="931ba-110">Бизнес-объекты, созданные в Microsoft Visual Basic могут автоматически помечены как "безопасные для скриптов" с помощью мастера пакета и развертывания.</span><span class="sxs-lookup"><span data-stu-id="931ba-110">Business objects created in Microsoft Visual Basic can be automatically marked as "safe for scripting" with the Package and Deployment Wizard.</span></span> <span data-ttu-id="931ba-111">Когда мастер просит указать параметры безопасности, выберите Сейф для инициализации и Сейф **сценариев.** </span><span class="sxs-lookup"><span data-stu-id="931ba-111">When the wizard asks you to specify safety settings, select **Safe for initialization** and **Safe for scripting**.</span></span>

<span data-ttu-id="931ba-112">На последнем шаге мастер установки приложений создает .htm и .cab файл.</span><span class="sxs-lookup"><span data-stu-id="931ba-112">On the last step, the Application Setup Wizard creates an .htm and a .cab file.</span></span> <span data-ttu-id="931ba-113">Затем можно скопировать эти два файла на целевой компьютер и дважды щелкнуть .htm файл, чтобы загрузить страницу и правильно зарегистрировать сервер.</span><span class="sxs-lookup"><span data-stu-id="931ba-113">You can then copy these two files to the target computer and double-click the .htm file to load the page and correctly register the server.</span></span>

<span data-ttu-id="931ba-114">Так как бизнес-объект будет установлен в каталоге Occache Windows System32 по умолчанию, переместите его в каталог Windows System32 и измените ключ реестра \\ \\ \\ **HKEY \_ CLASSES \_ ROOT \\ CLSID \\** \< *MyActiveXGUID* \> \\ **InprocServer32,** чтобы соответствовать правильному пути.</span><span class="sxs-lookup"><span data-stu-id="931ba-114">Because the business object will be installed in the Windows\\System32\\Occache directory by default, move it to the Windows\\System32 directory and change the **HKEY\_CLASSES\_ROOT\\CLSID\\**\<*MyActiveXGUID*\>\\**InprocServer32** registry key to match the correct path.</span></span>


> [!NOTE]
> <span data-ttu-id="931ba-115">Бизнес-объекты, помеченные как безопасные для создания сценариев или безопасные для инициализации, могут быть моментально и инициализированы любыми в сети.</span><span class="sxs-lookup"><span data-stu-id="931ba-115">Business objects marked as safe for scripting or safe for initialization can be instantiated and initialized by anyone over the network.</span></span> <span data-ttu-id="931ba-116">Любой настраиваемый бизнес-объект не должен быть разработан и реализован случайно.</span><span class="sxs-lookup"><span data-stu-id="931ba-116">Any custom business object must not be designed and implemented casually.</span></span> <span data-ttu-id="931ba-117">Крайне важно, чтобы такие объекты не представляют угрозы безопасности, которую хакеры могут исследовать, чтобы получить доступ к конфиденциальной области хостинг-сервера и нанести ущерб.</span><span class="sxs-lookup"><span data-stu-id="931ba-117">It is imperative that such objects do not present a security threat that hackers can explore to gain access to the sensitive area of the hosting server and inflict damages.</span></span>


