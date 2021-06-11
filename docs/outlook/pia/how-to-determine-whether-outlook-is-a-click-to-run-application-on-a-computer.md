---
title: Определение, является ли Outlook на компьютере приложением "нажми и работай"
TOCTitle: Determine whether Outlook is a Click-to-Run application on a computer
ms:assetid: 1b8573be-8ea8-4973-869d-87fda57ce525
ms:mtpsurl: https://msdn.microsoft.com/library/Ff522355(v=office.15)
ms:contentKeyID: 55119804
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a710baa4d70ac69b67d2a06fe694998884fd835
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356408"
---
# <a name="determine-whether-outlook-is-a-click-to-run-application-on-a-computer"></a><span data-ttu-id="c901d-102">Определение, является ли Outlook на компьютере приложением "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="c901d-102">Determine whether Outlook is a Click-to-Run application on a computer</span></span>

<span data-ttu-id="c901d-103">"Нажми и работай" — это механизм получения и обновления программ, доступный в Office 2010 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="c901d-103">Click-to-Run is a software delivery and updating mechanism available to Office 2010 and later versions.</span></span> <span data-ttu-id="c901d-104">Продукты, установленные с помощью технологии "нажми и работай", выполняются в виртуальной среде приложений локальной операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c901d-104">Products delivered via Click-to-Run execute in a virtual application environment on the local operating system.</span></span> <span data-ttu-id="c901d-105">Это означает, что в них используются закрытые копии файлов и параметров, а все внесенные ими изменения перехватываются в виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="c901d-105">This means that they have private copies of their files and settings, and that any changes they make are captured in the virtual environment.</span></span>

<span data-ttu-id="c901d-106">Технология "нажми и работай" позволяет пользователям быстрее начинать работу с приложением, не дожидаясь полного завершения установки продукта.</span><span class="sxs-lookup"><span data-stu-id="c901d-106">Click-to-Run is fast—users can start running an application within a short time without waiting for the complete product to finish installing.</span></span> <span data-ttu-id="c901d-107">Обновления выполняются автоматически в фоновом режиме, не требуя от пользователя сначала удалить установленный экземпляр или вручную установить обновления.</span><span class="sxs-lookup"><span data-stu-id="c901d-107">Updates are run automatically in the background, without requiring a user to first remove an installation or manually install updates.</span></span> <span data-ttu-id="c901d-108">Продукты, поддерживающие технологию "нажми и работай", являются виртуальными и не конфликтуют с другими установленными приложениями.</span><span class="sxs-lookup"><span data-stu-id="c901d-108">Click-to-Run products are virtualized and do not conflict with other installed software.</span></span> <span data-ttu-id="c901d-109">Но поскольку продукт, установленный с помощью технологии "нажми и работай", содержит закрытые копии всех файлов и регистрации, разработчик надстройки не может определить наличие продукта тем же способом, как при установке на жестком диске клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="c901d-109">However, because a product delivered by Click-to-Run has private copies of all its files and registration, an add-in developer cannot determine the product’s existence in the same manner as a product that was installed on a client computer’s hard disk.</span></span> <span data-ttu-id="c901d-110">Начиная с Outlook 2010, разработчики надстроек должны проверять, установлен ли экземпляр Outlook и использовалась ли для установки технология "нажми и работай".</span><span class="sxs-lookup"><span data-stu-id="c901d-110">Starting with Outlook 2010, add-in developers should verify whether Outlook has been installed, and whether Outlook has been delivered as a Click-to-Run product.</span></span>


> [!NOTE]
> <span data-ttu-id="c901d-111">В виртуальной среде приложения "нажми и работай" поддерживается только 32-разрядная версия Office 2013, даже если компьютер клиента работает под управлением 64-разрядной операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c901d-111">Only 32-bit Office 2013 is supported in the Click-to-Run virtual application environment, even if the client computer runs a 64-bit operating system.</span></span>



### <a name="to-check-whether-outlook-2013-was-delivered-by-click-to-run-on-a-client-computer"></a><span data-ttu-id="c901d-112">Чтобы проверить, установлен ли Outlook 2013 на компьютере клиента по технологии "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="c901d-112">To check whether Outlook 2013 was delivered by Click-to-Run on a client computer</span></span>

- <span data-ttu-id="c901d-113">подтвердите, существует ли раздел VirtualOutlook в следующем расположении реестра Windows:</span><span class="sxs-lookup"><span data-stu-id="c901d-113">Verify whether the VirtualOutlook key exists in the following location in the Windows registry:</span></span>
    
  `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
    
  <span data-ttu-id="c901d-114">Раздел VirtualOutlook является значением типа REG\_SZ, которое содержит тег языка установленного продукта, такой как "en-us".</span><span class="sxs-lookup"><span data-stu-id="c901d-114">The VirtualOutlook key is a REG\_SZ value that contains the culture tag of the installed product language, such as "en-us".</span></span>

## <a name="see-also"></a><span data-ttu-id="c901d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="c901d-115">See also</span></span>

- [<span data-ttu-id="c901d-116">Администрирование надстроек</span><span class="sxs-lookup"><span data-stu-id="c901d-116">Add-in administration</span></span>](add-in-administration.md)

