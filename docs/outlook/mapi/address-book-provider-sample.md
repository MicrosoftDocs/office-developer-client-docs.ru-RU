---
title: Пример поставщика адресной книги
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394722"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="2630c-103">Пример поставщика адресной книги</span><span class="sxs-lookup"><span data-stu-id="2630c-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="2630c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2630c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2630c-105">В этом примере поддерживает один контейнер только для чтения отображаемые имена и адреса электронной почты, которые читают плоской двоичных файлов.</span><span class="sxs-lookup"><span data-stu-id="2630c-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="2630c-106">В примере поддерживается одноразовых шаблоны и все параметры конфигурации, кроме мастер профилей.</span><span class="sxs-lookup"><span data-stu-id="2630c-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="2630c-107">В этом примере можно загрузить из [Примеры кода Outlook системы обмена сообщениями API (MAPI)](https://go.microsoft.com/fwlink/?LinkId=129740
).</span><span class="sxs-lookup"><span data-stu-id="2630c-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2630c-108">Исполняемый файл:</span><span class="sxs-lookup"><span data-stu-id="2630c-108">Executable:</span></span>  <br/> |<span data-ttu-id="2630c-109">SABP32.dll</span><span class="sxs-lookup"><span data-stu-id="2630c-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="2630c-110">Каталог исходного кода:</span><span class="sxs-lookup"><span data-stu-id="2630c-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="2630c-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="2630c-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="2630c-112">Язык:</span><span class="sxs-lookup"><span data-stu-id="2630c-112">Language:</span></span>  <br/> |<span data-ttu-id="2630c-113">C++</span><span class="sxs-lookup"><span data-stu-id="2630c-113">C++</span></span>  <br/> |
|<span data-ttu-id="2630c-114">Платформы:</span><span class="sxs-lookup"><span data-stu-id="2630c-114">Platforms:</span></span>  <br/> |<span data-ttu-id="2630c-115">Microsoft Visual Studio 2008 для компиляции для Windows Vista, Windows Server 2008, Windows XP с пакетом обновления 2 и Windows Server 2003 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="2630c-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="2630c-116">Поддерживаемые функции</span><span class="sxs-lookup"><span data-stu-id="2630c-116">Supported Features</span></span>

<span data-ttu-id="2630c-117">В этом примере не поддерживают следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="2630c-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="2630c-118">В таблице ограничений.</span><span class="sxs-lookup"><span data-stu-id="2630c-118">Table restrictions.</span></span> <span data-ttu-id="2630c-119">В примере реализуется соответствие префикса и неоднозначное имя разрешения.</span><span class="sxs-lookup"><span data-stu-id="2630c-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="2630c-120">Не реализует полный языковой ограничений MAPI и ограничения поддерживаются только на отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="2630c-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="2630c-121">Таблица отображения сведений для обмена сообщениями пользователи.</span><span class="sxs-lookup"><span data-stu-id="2630c-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="2630c-122">Одноразовых адреса.</span><span class="sxs-lookup"><span data-stu-id="2630c-122">One-off addresses.</span></span>
    
- <span data-ttu-id="2630c-123">Диалоговое окно "Расширенный поиск".</span><span class="sxs-lookup"><span data-stu-id="2630c-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="2630c-124">[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2630c-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="2630c-125">Этот интерфейс частично поддерживается; его методы **IMAPIProp** делегируются интерфейс **IPropData** .</span><span class="sxs-lookup"><span data-stu-id="2630c-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="2630c-126">Дополнительные сведения можно [IPropData: IMAPIProp](ipropdataimapiprop.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2630c-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="2630c-127">Интерактивные и программный конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2630c-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="2630c-128">Неподдерживаемые возможности</span><span class="sxs-lookup"><span data-stu-id="2630c-128">Unsupported Features</span></span>

<span data-ttu-id="2630c-129">В этом примере не поддерживает следующие функции:</span><span class="sxs-lookup"><span data-stu-id="2630c-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="2630c-130">Сортировка.</span><span class="sxs-lookup"><span data-stu-id="2630c-130">Sorting.</span></span>
    
- <span data-ttu-id="2630c-131">Списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="2630c-131">Distribution lists.</span></span>
    
- <span data-ttu-id="2630c-132">Создание, удаление и изменение записей.</span><span class="sxs-lookup"><span data-stu-id="2630c-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="2630c-133">Свойства с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="2630c-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="2630c-134">Именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2630c-134">Named properties.</span></span>
    
- <span data-ttu-id="2630c-135">Отличия между имени и фамилии в отображаемые имена.</span><span class="sxs-lookup"><span data-stu-id="2630c-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="2630c-136">**Установка примера поставщика адресной книги**</span><span class="sxs-lookup"><span data-stu-id="2630c-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="2630c-137">Чтобы загрузить образец поставщик адресной книги, обратитесь к разделу [Загрузка примеров Outlook MAPI](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="2630c-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="2630c-138">Найдите папку, в которой вы сохранили примеры Outlook MAPI.</span><span class="sxs-lookup"><span data-stu-id="2630c-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="2630c-139">Щелкните правой кнопкой мыши \*\*OutlookMAPISamples -\<номер версии\> \*\* ZIP-папку и выберите команду **Извлечь все**.</span><span class="sxs-lookup"><span data-stu-id="2630c-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="2630c-140">Нажмите кнопку **Обзор**, выберите расположение, где требуется сохранить образца и нажмите кнопку **извлечь**.</span><span class="sxs-lookup"><span data-stu-id="2630c-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="2630c-141">Запустите Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="2630c-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="2630c-142">В Visual Studio 2008 откройте меню **файл**, выберите команду **Открыть**и щелкните **Проект/решение**.</span><span class="sxs-lookup"><span data-stu-id="2630c-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="2630c-143">Перейдите к папке, в которой вы сохранили примера **SABP.vcproj**и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="2630c-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="2630c-144">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="2630c-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="2630c-145">В диалоговом окне **Сохранение файла** нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2630c-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="2630c-146">В папке, где был сохранен примера щелкните правой кнопкой мыши файл **install.bat** и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="2630c-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="2630c-147">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="2630c-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2630c-148">**Install.bat** копирует DLL-файл в папке установки Microsoft Office по умолчанию C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="2630c-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="2630c-149">Если вы установили продукты Office в другом месте, щелкните правой кнопкой мыши **Install.bat** и нажмите кнопку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="2630c-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="2630c-150">Файл открывается в "Блокнот".</span><span class="sxs-lookup"><span data-stu-id="2630c-150">The file opens in Notepad.</span></span> <span data-ttu-id="2630c-151">Замените путь установки по умолчанию путь установки, используемые на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="2630c-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

