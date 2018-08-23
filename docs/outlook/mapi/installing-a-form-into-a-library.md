---
title: Установка формы в библиотеке
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d3b20c9fb4b4f1a26eb4ed1a9a498bd56a915a70
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579783"
---
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="74e27-103">Установка формы в библиотеке</span><span class="sxs-lookup"><span data-stu-id="74e27-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="74e27-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74e27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74e27-105">Диспетчер формы MAPI по умолчанию, предоставленные с помощью пакета SDK Windows не предоставляет интерфейс пользователя для установки форм в различные библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="74e27-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="74e27-106">Таким образом, необходимо создать небольшое приложение — или подробное описание набор инструкций —, что пользователи могут использовать для установки формы.</span><span class="sxs-lookup"><span data-stu-id="74e27-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="74e27-107">При реализации приложения установки серию действий его необходимо выполнить для установки формы в таблице доступны следующие связанные содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="74e27-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="74e27-108">Вызовите функцию [MAPIOpenFormMgr](mapiopenformmgr.md) для открытия формы manager.</span><span class="sxs-lookup"><span data-stu-id="74e27-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="74e27-109">Используйте метод [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) или [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) для выбора и откройте конечный контейнер для формы.</span><span class="sxs-lookup"><span data-stu-id="74e27-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="74e27-110">Используйте функцию [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) для установки формы.</span><span class="sxs-lookup"><span data-stu-id="74e27-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="74e27-111">Для установки в библиотеке форм локального приведены шаги с 4 по 6.</span><span class="sxs-lookup"><span data-stu-id="74e27-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="74e27-112">Скопируйте все файлы в соответствующее место на локальном диске, если установлена в локальной форме библиотеку на рабочей станции пользователя.</span><span class="sxs-lookup"><span data-stu-id="74e27-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="74e27-113">При необходимости измените файл конфигурации формы в соответствии с текущим путям компонентов.</span><span class="sxs-lookup"><span data-stu-id="74e27-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="74e27-114">Файл конфигурации форма может содержать относительные пути, в противном случае это действие можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="74e27-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="74e27-115">Выполните соответствующие операции регистрации OLE для связи с сервером формы установлен тип сообщения.</span><span class="sxs-lookup"><span data-stu-id="74e27-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="74e27-116">Если форма была установлена в локальной форме библиотеку, скопируйте в форме (ICO) и файлы конфигурации (.cfg) в каталог %WINDOWS%\FORMS\CONFIGS чтобы формы можно автоматически восстановить в случае библиотека форм повреждена или удалена.</span><span class="sxs-lookup"><span data-stu-id="74e27-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="74e27-117">Этот шаг не рекомендуется, но не обязательно.</span><span class="sxs-lookup"><span data-stu-id="74e27-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="74e27-118">Можно упростить установку в локальной библиотеке, заменив шаги 1 и 2 вызова функции [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="74e27-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="74e27-119">См. также</span><span class="sxs-lookup"><span data-stu-id="74e27-119">See also</span></span>



[<span data-ttu-id="74e27-120">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="74e27-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

