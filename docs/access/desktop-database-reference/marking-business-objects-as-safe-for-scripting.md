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
# <a name="marking-business-objects-as-safe-for-scripting"></a><span data-ttu-id="ccaeb-102">Пометка бизнес-объектов как безопасных для написания скриптов</span><span class="sxs-lookup"><span data-stu-id="ccaeb-102">Marking business objects as safe for scripting</span></span>

<span data-ttu-id="ccaeb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ccaeb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ccaeb-104">Чтобы обеспечить безопасность Интернет-среды, необходимо пометить все бизнес-объекты, создаваемые с помощью [RDS. ](dataspace-object-rds.md)Метод [CreateObject](createobject-method-rds.md) объекта Space в качестве "безопасного для скриптов".</span><span class="sxs-lookup"><span data-stu-id="ccaeb-104">To help ensure a secure Internet environment, you need to mark any business objects instantiated with the [RDS.DataSpace](dataspace-object-rds.md) object's [CreateObject](createobject-method-rds.md) method as "safe for scripting."</span></span> <span data-ttu-id="ccaeb-105">Чтобы их можно было использовать в DCOM, необходимо убедиться, что они отмечены в области лицензирования системного реестра.</span><span class="sxs-lookup"><span data-stu-id="ccaeb-105">You need to ensure they are marked as such in the License area of the system registry before they can be used in DCOM.</span></span>

<span data-ttu-id="ccaeb-106">Чтобы вручную пометить бизнес-объект как безопасный для написания скриптов, создайте текстовый файл с расширением REG, содержащим следующий текст.</span><span class="sxs-lookup"><span data-stu-id="ccaeb-106">To manually mark your business object as safe for scripting, create a text file with a .reg extension that contains the following text.</span></span> <span data-ttu-id="ccaeb-107">Следующие два номера включают функцию безопасного для скриптов:</span><span class="sxs-lookup"><span data-stu-id="ccaeb-107">The following two numbers enable the safe-for-scripting feature:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

<span data-ttu-id="ccaeb-108">где \< *мяктивексгуид* \> — это шестнадцатеричный идентификатор GUID вашего бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="ccaeb-108">where \<*MyActiveXGUID*\> is the hexadecimal GUID number of your business object.</span></span> <span data-ttu-id="ccaeb-109">Сохраните его и объедините в реестр с помощью редактора реестра или двойным щелчком REG файла в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="ccaeb-109">Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</span></span>

<span data-ttu-id="ccaeb-110">Бизнес-объекты, созданные в Microsoft Visual Basic, можно автоматически пометить как "безопасные для скриптов" с помощью мастера упаковки и развертывания.</span><span class="sxs-lookup"><span data-stu-id="ccaeb-110">Business objects created in Microsoft Visual Basic can be automatically marked as "safe for scripting" with the Package and Deployment Wizard.</span></span> <span data-ttu-id="ccaeb-111">Когда мастер запросит параметры безопасности, выберите **безопасный для инициализации** и **безопасного для сценариев**.</span><span class="sxs-lookup"><span data-stu-id="ccaeb-111">When the wizard asks you to specify safety settings, select **Safe for initialization** and **Safe for scripting**.</span></span>

<span data-ttu-id="ccaeb-112">На последнем шаге мастер установки приложений создает htm-и CAB-файлы.</span><span class="sxs-lookup"><span data-stu-id="ccaeb-112">On the last step, the Application Setup Wizard creates an .htm and a .cab file.</span></span> <span data-ttu-id="ccaeb-113">Затем можно скопировать эти два файла на конечный компьютер и дважды щелкнуть htm-файл, чтобы загрузить страницу и правильно зарегистрировать сервер.</span><span class="sxs-lookup"><span data-stu-id="ccaeb-113">You can then copy these two files to the target computer and double-click the .htm file to load the page and correctly register the server.</span></span>

<span data-ttu-id="ccaeb-114">Так как бизнес-объект будет установлен в каталог Windows\\system32\\Occache по умолчанию, переместите его в каталог System32\\Windows и измените раздел реестра\<*мяктивексгуид*\>\\**InprocServer32** **корневого\\\_\\CLSID для классов hKey\_**, чтобы соответствовать правильному пути.</span><span class="sxs-lookup"><span data-stu-id="ccaeb-114">Because the business object will be installed in the Windows\\System32\\Occache directory by default, move it to the Windows\\System32 directory and change the **HKEY\_CLASSES\_ROOT\\CLSID\\**\<*MyActiveXGUID*\>\\**InprocServer32** registry key to match the correct path.</span></span>


> [!NOTE]
> <span data-ttu-id="ccaeb-115">Экземпляры бизнес-объектов, помеченных как безопасные для выполнения скриптов или для инициализации, могут быть созданы и инициализированы кем-то через сеть.</span><span class="sxs-lookup"><span data-stu-id="ccaeb-115">Business objects marked as safe for scripting or safe for initialization can be instantiated and initialized by anyone over the network.</span></span> <span data-ttu-id="ccaeb-116">Любой настраиваемый бизнес-объект не должен разрабатываться и реализовываться в случайном виде.</span><span class="sxs-lookup"><span data-stu-id="ccaeb-116">Any custom business object must not be designed and implemented casually.</span></span> <span data-ttu-id="ccaeb-117">Крайне важно, чтобы такие объекты не представлю угрозу безопасности, которые могут быть проучены хакерами, чтобы получить доступ к конфиденциальной области сервера хостинга и ущерба инфликт.</span><span class="sxs-lookup"><span data-stu-id="ccaeb-117">It is imperative that such objects do not present a security threat that hackers can explore to gain access to the sensitive area of the hosting server and inflict damages.</span></span>


