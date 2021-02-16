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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331110"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="b72bc-103">Пример поставщика адресной книги</span><span class="sxs-lookup"><span data-stu-id="b72bc-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="b72bc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b72bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b72bc-105">В этом примере поддерживается один контейнер только для чтения для отображаемого имени и адресов электронной почты, которые считыются из плоского двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="b72bc-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="b72bc-106">Пример поддерживает однонакладные шаблоны и все параметры конфигурации, кроме мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="b72bc-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="b72bc-107">Вы можете скачать этот пример из примеров кода для API сообщений [Outlook (MAPI).](https://go.microsoft.com/fwlink/?LinkId=129740
)</span><span class="sxs-lookup"><span data-stu-id="b72bc-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b72bc-108">Исполняемый исполня</span><span class="sxs-lookup"><span data-stu-id="b72bc-108">Executable:</span></span>  <br/> |<span data-ttu-id="b72bc-109">SABP32.dll</span><span class="sxs-lookup"><span data-stu-id="b72bc-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="b72bc-110">Каталог с исходным кодом:</span><span class="sxs-lookup"><span data-stu-id="b72bc-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="b72bc-111">SampleAddressBookProvider\SABP</span><span class="sxs-lookup"><span data-stu-id="b72bc-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="b72bc-112">Язык:</span><span class="sxs-lookup"><span data-stu-id="b72bc-112">Language:</span></span>  <br/> |<span data-ttu-id="b72bc-113">C++</span><span class="sxs-lookup"><span data-stu-id="b72bc-113">C++</span></span>  <br/> |
|<span data-ttu-id="b72bc-114">Платформы:</span><span class="sxs-lookup"><span data-stu-id="b72bc-114">Platforms:</span></span>  <br/> |<span data-ttu-id="b72bc-115">Microsoft Visual Studio 2008 для Windows Vista, Windows Server 2008, Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="b72bc-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="b72bc-116">Поддерживаемые функции</span><span class="sxs-lookup"><span data-stu-id="b72bc-116">Supported Features</span></span>

<span data-ttu-id="b72bc-117">В этом примере поддерживаются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="b72bc-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="b72bc-118">Ограничения таблиц.</span><span class="sxs-lookup"><span data-stu-id="b72bc-118">Table restrictions.</span></span> <span data-ttu-id="b72bc-119">В примере реализованы префикс-совпадение и разрешение неоднозначных имен.</span><span class="sxs-lookup"><span data-stu-id="b72bc-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="b72bc-120">Он не реализует полный язык ограничений MAPI, и ограничения поддерживаются только для отображаемого имени.</span><span class="sxs-lookup"><span data-stu-id="b72bc-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="b72bc-121">Отображаемая таблица сведений для пользователей сообщений.</span><span class="sxs-lookup"><span data-stu-id="b72bc-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="b72bc-122">Одновключные адреса.</span><span class="sxs-lookup"><span data-stu-id="b72bc-122">One-off addresses.</span></span>
    
- <span data-ttu-id="b72bc-123">Диалоговое окно "Расширенный поиск".</span><span class="sxs-lookup"><span data-stu-id="b72bc-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="b72bc-124">Интерфейс [IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="b72bc-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="b72bc-125">Этот интерфейс частично поддерживается; Методы **IMAPIProp** делегироваться **интерфейсу IPropData.**</span><span class="sxs-lookup"><span data-stu-id="b72bc-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="b72bc-126">Дополнительные сведения см. в интерфейсе [IPropData : IMAPIProp.](ipropdataimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="b72bc-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="b72bc-127">Интерактивная и программная конфигурация.</span><span class="sxs-lookup"><span data-stu-id="b72bc-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="b72bc-128">Неподтверченные функции</span><span class="sxs-lookup"><span data-stu-id="b72bc-128">Unsupported Features</span></span>

<span data-ttu-id="b72bc-129">В этом примере не поддерживаются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="b72bc-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="b72bc-130">Сортировка.</span><span class="sxs-lookup"><span data-stu-id="b72bc-130">Sorting.</span></span>
    
- <span data-ttu-id="b72bc-131">Списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="b72bc-131">Distribution lists.</span></span>
    
- <span data-ttu-id="b72bc-132">Создание, удаление и изменение записей.</span><span class="sxs-lookup"><span data-stu-id="b72bc-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="b72bc-133">Свойства с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="b72bc-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="b72bc-134">Именуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="b72bc-134">Named properties.</span></span>
    
- <span data-ttu-id="b72bc-135">Различие между именами и фамилиями в отображаемом имени.</span><span class="sxs-lookup"><span data-stu-id="b72bc-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="b72bc-136">**Установка примера поставщика адресной книги**</span><span class="sxs-lookup"><span data-stu-id="b72bc-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="b72bc-137">Чтобы скачать пример поставщика адресной книги, скачайте примеры [OUTLOOK MAPI.](downloading-the-outlook-mapi-samples.md)</span><span class="sxs-lookup"><span data-stu-id="b72bc-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="b72bc-138">Найдите папку, в которой сохранены примеры MAPI для Outlook.</span><span class="sxs-lookup"><span data-stu-id="b72bc-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="b72bc-139">Щелкните правой кнопкой **мыши ZIP-папку OutlookMAPISamples версии \< \>** и выберите **"Извлечь все".**</span><span class="sxs-lookup"><span data-stu-id="b72bc-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="b72bc-140">Нажмите **кнопку**"Обзор", выберите расположение, в котором вы хотите сохранить пример, и нажмите кнопку **"Извлечь".**</span><span class="sxs-lookup"><span data-stu-id="b72bc-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="b72bc-141">Запустите Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="b72bc-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="b72bc-142">В Visual Studio 2008 выберите **"Файл",** **"Открыть"** и **"Проект/решение".**</span><span class="sxs-lookup"><span data-stu-id="b72bc-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="b72bc-143">Перейдите к расположению, в котором сохранен пример, нажмите **кнопку SABP.vcproj** и нажмите кнопку **"Открыть".**</span><span class="sxs-lookup"><span data-stu-id="b72bc-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="b72bc-144">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="b72bc-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="b72bc-145">В **диалоговом окне** "Сохранить файл как" нажмите кнопку **"Сохранить".**</span><span class="sxs-lookup"><span data-stu-id="b72bc-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="b72bc-146">В папке, в которой сохранен пример, щелкните правой кнопкой мыши файлinstall.bat **и** выберите "Запуск от прав **администратора".**</span><span class="sxs-lookup"><span data-stu-id="b72bc-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="b72bc-147">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="b72bc-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b72bc-148">**Install.bat** DLL-файл копируется в папку установки Microsoft Office по умолчанию C:\Program Files\Microsoft Office\Office12.\.</span><span class="sxs-lookup"><span data-stu-id="b72bc-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="b72bc-149">Если продукты Office установлены в другом расположении, щелкните правой кнопкой мышиInstall.bat **и** выберите **"Изменить".**</span><span class="sxs-lookup"><span data-stu-id="b72bc-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="b72bc-150">Файл откроется в Блокноте.</span><span class="sxs-lookup"><span data-stu-id="b72bc-150">The file opens in Notepad.</span></span> <span data-ttu-id="b72bc-151">Замените путь установки по умолчанию на путь установки, используемый на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b72bc-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

