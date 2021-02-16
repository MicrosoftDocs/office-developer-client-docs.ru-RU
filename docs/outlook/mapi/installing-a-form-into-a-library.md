---
title: Установка формы в библиотеку
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 08470a80153e42136922ae502252d83de0125512
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433145"
---
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="ec417-103">Установка формы в библиотеку</span><span class="sxs-lookup"><span data-stu-id="ec417-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="ec417-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec417-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec417-105">Диспетчер форм MAPI по умолчанию, поставляющийся с Windows SDK, не предоставляет пользовательский интерфейс для установки форм в различных библиотеках форм.</span><span class="sxs-lookup"><span data-stu-id="ec417-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="ec417-106">По этой причине необходимо создать небольшое приложение (или подробный набор инструкций), которое пользователи могут использовать для установки формы.</span><span class="sxs-lookup"><span data-stu-id="ec417-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="ec417-107">При реализации приложения установки необходимо выполнить ряд действий для установки формы в связанную с папкой таблицу содержимого следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ec417-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="ec417-108">Вызовите [функцию MAPIOpenFormMgr,](mapiopenformmgr.md) чтобы открыть диспетчер форм.</span><span class="sxs-lookup"><span data-stu-id="ec417-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="ec417-109">Используйте [метод IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) или [IMAPIFormMgr::SelectFormContainer,](imapiformmgr-selectformcontainer.md) чтобы выбрать и открыть целевой контейнер для формы.</span><span class="sxs-lookup"><span data-stu-id="ec417-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="ec417-110">Используйте [функцию IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) для установки формы.</span><span class="sxs-lookup"><span data-stu-id="ec417-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="ec417-111">Шаги 4–6 для установки в локализованную библиотеку форм:</span><span class="sxs-lookup"><span data-stu-id="ec417-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="ec417-112">Скопируйте все файлы в нужное место на локальном диске, если установка происходит в локализованную библиотеку форм на рабочей станции пользователя.</span><span class="sxs-lookup"><span data-stu-id="ec417-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="ec417-113">При необходимости измените файл конфигурации формы, чтобы отразить текущие пути компонентов.</span><span class="sxs-lookup"><span data-stu-id="ec417-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="ec417-114">Файл конфигурации формы может содержать относительные пути, в этом случае этот шаг может не потребоваться.</span><span class="sxs-lookup"><span data-stu-id="ec417-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="ec417-115">Выполните соответствующие действия регистрации OLE, чтобы связать тип сообщения с устанавливаемого сервера форм.</span><span class="sxs-lookup"><span data-stu-id="ec417-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="ec417-116">Если форма была установлена в локальной библиотеке форм, скопируйте файлы значка формы (.ico) и файлов конфигурации (CFG) в каталог %WINDOWS%\FORMS\CONFIGS, чтобы ее можно было автоматически восстановить на случай, если библиотека форм повреждена или удалена.</span><span class="sxs-lookup"><span data-stu-id="ec417-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="ec417-117">Этот шаг рекомендуется, но не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="ec417-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ec417-118">Вы можете упростить установку в локальной библиотеке форм, заменив шаги 1 и 2 вызовом функции [MAPIOpenLocalFormContainer.](mapiopenlocalformcontainer.md)</span><span class="sxs-lookup"><span data-stu-id="ec417-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ec417-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ec417-119">See also</span></span>



[<span data-ttu-id="ec417-120">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="ec417-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

