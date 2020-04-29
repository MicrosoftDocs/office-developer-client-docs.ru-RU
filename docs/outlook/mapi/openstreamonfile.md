---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b05f5b30eceb7df1bed76c64f4bdda87ede0e463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439095"
---
# <a name="openstreamonfile"></a><span data-ttu-id="99017-103">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="99017-103">OpenStreamOnFile</span></span>

  
  
<span data-ttu-id="99017-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99017-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99017-105">Выделяет и инициализирует объект OLE **IStream** для доступа к содержимому файла.</span><span class="sxs-lookup"><span data-stu-id="99017-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="99017-106">Эта функция принимает строку ANSI в качестве имени файла, включая путь и расширение файла, поэтому рекомендуется использовать версию этой функции ( [опенстреамонфилев](openstreamonfilew.md)) в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="99017-106">This function takes an ANSI string as the file name including the path and the file extension, therefore, use of the Unicode version of this function, [OpenStreamOnFileW](openstreamonfilew.md), is recommended.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="99017-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="99017-107">Header file:</span></span>  <br/> |<span data-ttu-id="99017-108">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="99017-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="99017-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="99017-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="99017-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="99017-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="99017-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="99017-111">Called by:</span></span>  <br/> |<span data-ttu-id="99017-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="99017-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="99017-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="99017-113">Parameters</span></span>

 <span data-ttu-id="99017-114">_лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="99017-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="99017-115">возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="99017-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="99017-116">_лпфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="99017-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="99017-117">возврата Указатель на функцию [мапифрибуффер](mapifreebuffer.md) , который будет использоваться для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="99017-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="99017-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99017-118">_ulFlags_</span></span>
  
> <span data-ttu-id="99017-119">возврата Битовая маска флагов, используемых для управления созданием или открытием файла, к которому можно получить доступ через объект OLE **IStream** .</span><span class="sxs-lookup"><span data-stu-id="99017-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="99017-120">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="99017-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="99017-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="99017-121">SOF_UNIQUEFILENAME</span></span> 
  
> <span data-ttu-id="99017-122">Для объекта **IStream** будет создан временный файл.</span><span class="sxs-lookup"><span data-stu-id="99017-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="99017-123">Если этот флаг установлен, также должны быть заданы флаги STGM_CREATE и STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="99017-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="99017-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="99017-124">STGM_CREATE</span></span> 
  
> <span data-ttu-id="99017-125">Файл будет создан, даже если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="99017-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="99017-126">Если параметр _лпсзфиленаме_ не задан, то этот флаг и STGM_DELETEONRELEASE должны быть установлены.</span><span class="sxs-lookup"><span data-stu-id="99017-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="99017-127">Если параметр STGM_CREATE установлен, также должен быть установлен флаг STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="99017-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="99017-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="99017-128">STGM_DELETEONRELEASE</span></span> 
  
> <span data-ttu-id="99017-129">Файл будет удален при отпускании объекта **IStream** .</span><span class="sxs-lookup"><span data-stu-id="99017-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="99017-130">Если параметр _лпсзфиленаме_ не задан, то этот флаг и STGM_CREATE должны быть установлены.</span><span class="sxs-lookup"><span data-stu-id="99017-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="99017-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="99017-131">STGM_READ</span></span> 
  
> <span data-ttu-id="99017-132">Файл будет создан или открыт с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="99017-132">The file is to be created or opened with read-only access.</span></span> 
    
<span data-ttu-id="99017-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="99017-133">STGM_READWRITE</span></span> 
  
> <span data-ttu-id="99017-134">Файл будет создан или открыт с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="99017-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="99017-135">Если этот флаг не установлен, то флаг STGM_CREATE не должен быть установлен ни один из них.</span><span class="sxs-lookup"><span data-stu-id="99017-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span> 
    
 <span data-ttu-id="99017-136">_лпсзфиленаме_</span><span class="sxs-lookup"><span data-stu-id="99017-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="99017-137">возврата Имя файла, включая путь и расширение файла, для которого **опенстреамонфиле** Инициализирует объект **IStream** .</span><span class="sxs-lookup"><span data-stu-id="99017-137">[in] The filename, including path and extension, of the file for which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="99017-138">Если установлен флаг SOF_UNIQUEFILENAME, _лпсзфиленаме_ содержит путь к каталогу, в котором необходимо создать временный файл.</span><span class="sxs-lookup"><span data-stu-id="99017-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="99017-139">Если _лпсзфиленаме_ имеет значение null, **опенстреамонфиле** получает соответствующий путь из системы, и необходимо задать флаги STGM_CREATE и STGM_DELETEONRELEASE.</span><span class="sxs-lookup"><span data-stu-id="99017-139">If  _lpszFileName_ is NULL, **OpenStreamOnFile** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="99017-140">_лпсзпрефикс_</span><span class="sxs-lookup"><span data-stu-id="99017-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="99017-141">возврата Префикс имени файла, в котором **опенстреамонфиле** Инициализирует объект **IStream** .</span><span class="sxs-lookup"><span data-stu-id="99017-141">[in] The prefix for the filename on which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="99017-142">Если этот параметр установлен, префикс должен содержать не более трех символов.</span><span class="sxs-lookup"><span data-stu-id="99017-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="99017-143">Если _лпсзпрефикс_ имеет значение null, используется префикс "SOF".</span><span class="sxs-lookup"><span data-stu-id="99017-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="99017-144">_лппстреам_</span><span class="sxs-lookup"><span data-stu-id="99017-144">_lppStream_</span></span>
  
> <span data-ttu-id="99017-145">вышли Указатель на указатель на объект, который предоставляет интерфейс **IStream** .</span><span class="sxs-lookup"><span data-stu-id="99017-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="99017-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99017-146">Return value</span></span>

<span data-ttu-id="99017-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="99017-147">S_OK</span></span> 
  
> <span data-ttu-id="99017-148">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="99017-148">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="99017-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="99017-149">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="99017-150">Доступ к файлу невозможен из-за недостаточного разрешения пользователя или изменения файлов, доступных только для чтения.</span><span class="sxs-lookup"><span data-stu-id="99017-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span> 
    
<span data-ttu-id="99017-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="99017-151">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="99017-152">Указанный файл не существует.</span><span class="sxs-lookup"><span data-stu-id="99017-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99017-153">Примечания</span><span class="sxs-lookup"><span data-stu-id="99017-153">Remarks</span></span>

<span data-ttu-id="99017-154">Функция **опенстреамонфиле** имеет два важных применения, которые различаются по значению флага SOF_UNIQUEFILENAME.</span><span class="sxs-lookup"><span data-stu-id="99017-154">The **OpenStreamOnFile** function has two important uses, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="99017-155">Если этот флаг не задан, **опенстреамонфиле** открывает объект **IStream** в существующем файле, например, чтобы скопировать его содержимое в свойство **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) вложения, используя метод **IStream:: CopyTo** .</span><span class="sxs-lookup"><span data-stu-id="99017-155">When this flag is not set, **OpenStreamOnFile** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="99017-156">В этом случае параметр _лпсзфиленаме_ указывает путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="99017-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="99017-157">Когда SOF_UNIQUEFILENAME задается, **опенстреамонфиле** создает временный файл для хранения данных для объекта **IStream** .</span><span class="sxs-lookup"><span data-stu-id="99017-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFile** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="99017-158">В этом случае параметр _лпсзфиленаме_ может указать путь к каталогу, в котором будет создан файл, а параметр _лпсзпрефикс_ можно указать префикс для имени файла.</span><span class="sxs-lookup"><span data-stu-id="99017-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="99017-159">Когда вызывающий клиентское приложение или поставщик услуг завершает работу с объектом **IStream** , он должен освободить его, вызвав метод OLE **IStream:: Release** .</span><span class="sxs-lookup"><span data-stu-id="99017-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="99017-160">MAPI использует функции, на которые указывает _лпаллокатебуффер_ и _лпфрибуффер_ для большей части памяти и освобождений, в частности, для выделения памяти, используемой клиентскими приложениями при вызове интерфейсов объектов, таких как [IMAPIProp::/PROPS](imapiprop-getprops.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="99017-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="99017-161">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="99017-161">Notes to callers</span></span>

<span data-ttu-id="99017-162">Флаг SOF_UNIQUEFILENAME используется для создания временного файла с именем, уникальным для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="99017-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="99017-163">Если этот флаг установлен, параметр _лпсзфиленаме_ спеЦифес путь к временному файлу, а параметр _лпсзпрефикс_ содержит префиксные символы имени файла.</span><span class="sxs-lookup"><span data-stu-id="99017-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="99017-164">Сконструированное имя файла <prefix>— hhhh. TMP, где HHHH — это шестнадцатеричное число.</span><span class="sxs-lookup"><span data-stu-id="99017-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="99017-165">Если _лпсзфиленаме_ имеет значение null, файл будет создан во временном каталоге файлов, который возвращается из функции Windows **жеттемппас**, или из текущего каталога, если не указан временный каталог файлов.</span><span class="sxs-lookup"><span data-stu-id="99017-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span> 
  
<span data-ttu-id="99017-166">Если флаг SOF_UNIQUEFILENAME не установлен, то _лпсзпрефикс_ игнорируется и _лпсзфиленаме_ должен содержать полный путь и имя файла, который требуется открыть или создать.</span><span class="sxs-lookup"><span data-stu-id="99017-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="99017-167">Файл будет открыт или создан на основе других флагов, заданных в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="99017-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="99017-168">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="99017-168">MFCMAPI reference</span></span>

<span data-ttu-id="99017-169">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="99017-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="99017-170">**Файл**</span><span class="sxs-lookup"><span data-stu-id="99017-170">**File**</span></span>|<span data-ttu-id="99017-171">**Функция**</span><span class="sxs-lookup"><span data-stu-id="99017-171">**Function**</span></span>|<span data-ttu-id="99017-172">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="99017-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99017-173">Файл. cpp</span><span class="sxs-lookup"><span data-stu-id="99017-173">File.cpp</span></span>  <br/> |<span data-ttu-id="99017-174">вритеаттачстреамтофиле</span><span class="sxs-lookup"><span data-stu-id="99017-174">WriteAttachStreamToFile</span></span>  <br/> |<span data-ttu-id="99017-175">MFCMAPI использует метод **опенстреамонфиле** , чтобы открыть поток в файле, чтобы можно было записать вложение в него.</span><span class="sxs-lookup"><span data-stu-id="99017-175">MFCMAPI uses the **OpenStreamOnFile** method to open a stream on a file so an attachment can be written out to it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99017-176">См. также</span><span class="sxs-lookup"><span data-stu-id="99017-176">See also</span></span>



[<span data-ttu-id="99017-177">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="99017-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

