---
title: Пометка бизнес-объекты как безопасные для скриптов
TOCTitle: Marking business objects as safe for scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bfd2a93b4a228186629d0c08e26cf2b0b7b32804
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944258"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a><span data-ttu-id="6bc28-102">Пометка бизнес-объекты как безопасные для скриптов</span><span class="sxs-lookup"><span data-stu-id="6bc28-102">Marking business objects as safe for scripting</span></span>

<span data-ttu-id="6bc28-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6bc28-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6bc28-104">Чтобы обеспечить надлежащую безопасной среде Интернета, нужно пометить любой бизнес-объекты с [RDS. экземпляр Пространства данных](dataspace-object-rds.md) метод [CreateObject](createobject-method-rds.md) объекта как «безопасные для скриптов».</span><span class="sxs-lookup"><span data-stu-id="6bc28-104">To help ensure a secure Internet environment, you need to mark any business objects instantiated with the [RDS.DataSpace](dataspace-object-rds.md) object's [CreateObject](createobject-method-rds.md) method as "safe for scripting."</span></span> <span data-ttu-id="6bc28-105">Необходимо убедиться, что они помечены как таковым в области лицензии системного реестра перед их можно использовать в DCOM.</span><span class="sxs-lookup"><span data-stu-id="6bc28-105">You need to ensure they are marked as such in the License area of the system registry before they can be used in DCOM.</span></span>

<span data-ttu-id="6bc28-106">Чтобы вручную пометить бизнес-объекта как безопасные для скриптов, создайте текстовый файл с расширением REG, содержащий следующий текст.</span><span class="sxs-lookup"><span data-stu-id="6bc28-106">To manually mark your business object as safe for scripting, create a text file with a .reg extension that contains the following text.</span></span> <span data-ttu-id="6bc28-107">Следующие два номера включить функцию безопасного для использования в сценариях:</span><span class="sxs-lookup"><span data-stu-id="6bc28-107">The following two numbers enable the safe-for-scripting feature:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

<span data-ttu-id="6bc28-108">где \< *MyActiveXGUID* \> — это шестнадцатеричный номер GUID бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="6bc28-108">where \<*MyActiveXGUID*\> is the hexadecimal GUID number of your business object.</span></span> <span data-ttu-id="6bc28-109">Сохраните его и объединение его в реестр, с помощью редактора реестра или дважды щелкнув REG-файл в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="6bc28-109">Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</span></span>

<span data-ttu-id="6bc28-110">Бизнес-объекты, созданные в Microsoft Visual Basic может автоматически помечен как «безопасные для скриптов» с помощью мастера пакетов и развертывания.</span><span class="sxs-lookup"><span data-stu-id="6bc28-110">Business objects created in Microsoft Visual Basic can be automatically marked as "safe for scripting" with the Package and Deployment Wizard.</span></span> <span data-ttu-id="6bc28-111">Когда мастер спросит, можно использовать для определения параметров безопасности, выберите **безопасные для инициализации** и **безопасный для сценариев**.</span><span class="sxs-lookup"><span data-stu-id="6bc28-111">When the wizard asks you to specify safety settings, select **Safe for initialization** and **Safe for scripting**.</span></span>

<span data-ttu-id="6bc28-112">На последнем шаге мастера установки приложения создает файлов htm и в CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="6bc28-112">On the last step, the Application Setup Wizard creates an .htm and a .cab file.</span></span> <span data-ttu-id="6bc28-113">Затем можно скопировать эти файлы на целевом компьютере и дважды щелкните htm-файл для загрузки страницы и правильной регистрации сервера.</span><span class="sxs-lookup"><span data-stu-id="6bc28-113">You can then copy these two files to the target computer and double-click the .htm file to load the page and correctly register the server.</span></span>

<span data-ttu-id="6bc28-114">Так как бизнес-объект будет установлен в окнах\\System32\\Occache каталог по умолчанию, перетащить его в Windows\\каталог System32 и измените **HKEY\_КЛАССЫ\_КОРНЕВОЙ\\CLSID\\ \*\* \< *MyActiveXGUID*\>\\раздел реестра**InprocServer32\*\* в соответствии с правильный путь.</span><span class="sxs-lookup"><span data-stu-id="6bc28-114">Because the business object will be installed in the Windows\\System32\\Occache directory by default, move it to the Windows\\System32 directory and change the **HKEY\_CLASSES\_ROOT\\CLSID\\**\<*MyActiveXGUID*\>\\**InprocServer32** registry key to match the correct path.</span></span>


> [!NOTE]
> <span data-ttu-id="6bc28-115">Бизнес-объектов, помеченных как безопасные для использования или безопасные для инициализации можно создать экземпляр и инициализации кем-либо по сети.</span><span class="sxs-lookup"><span data-stu-id="6bc28-115">Business objects marked as safe for scripting or safe for initialization can be instantiated and initialized by anyone over the network.</span></span> <span data-ttu-id="6bc28-116">Любой пользовательский бизнес-объект должен не предназначена и реализации случайного.</span><span class="sxs-lookup"><span data-stu-id="6bc28-116">Any custom business object must not be designed and implemented casually.</span></span> <span data-ttu-id="6bc28-117">Крайне важно, что такие объекты, не представляют угрозы безопасности, злоумышленники могут просмотреть получить доступ к области конфиденциальных размещения сервера и оказать убытков.</span><span class="sxs-lookup"><span data-stu-id="6bc28-117">It is imperative that such objects do not present a security threat that hackers can explore to gain access to the sensitive area of the hosting server and inflict damages.</span></span>


