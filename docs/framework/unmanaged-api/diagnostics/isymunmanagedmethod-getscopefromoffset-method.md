---
title: "ISymUnmanagedMethod::GetScopeFromOffset 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedMethod.GetScopeFromOffset
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedMethod::GetScopeFromOffset
helpviewer_keywords:
- GetScopeFromOffset method [.NET Framework debugging]
- ISymUnmanagedMethod::GetScopeFromOffset method [.NET Framework debugging]
ms.assetid: d14cf210-81f8-46e1-8b19-6ddec0ba8b11
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: b863031cae487a2c081f23aeada1971893aa339f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedmethodgetscopefromoffset-method"></a><span data-ttu-id="ea8d7-102">ISymUnmanagedMethod::GetScopeFromOffset 方法</span><span class="sxs-lookup"><span data-stu-id="ea8d7-102">ISymUnmanagedMethod::GetScopeFromOffset Method</span></span>
<span data-ttu-id="ea8d7-103">获取在此方法包含给定的偏移量内最封闭的词法范围。</span><span class="sxs-lookup"><span data-stu-id="ea8d7-103">Gets the most enclosing lexical scope within this method that encloses the given offset.</span></span> <span data-ttu-id="ea8d7-104">这可以用于启动本地变量的搜索。</span><span class="sxs-lookup"><span data-stu-id="ea8d7-104">This can be used to start local variable searches.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea8d7-105">语法</span><span class="sxs-lookup"><span data-stu-id="ea8d7-105">Syntax</span></span>  
  
```  
HRESULT GetScopeFromOffset(  
    [in]  ULONG32 offset,  
    [out, retval] ISymUnmanagedScope**  pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ea8d7-106">参数</span><span class="sxs-lookup"><span data-stu-id="ea8d7-106">Parameters</span></span>  
 `offset`  
 <span data-ttu-id="ea8d7-107">[in]A`ULONG`包含的偏移量。</span><span class="sxs-lookup"><span data-stu-id="ea8d7-107">[in] A `ULONG` that contains the offset.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="ea8d7-108">[out]一个指针，它设置为返回[ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)接口。</span><span class="sxs-lookup"><span data-stu-id="ea8d7-108">[out] A pointer that is set to the returned [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ea8d7-109">返回值</span><span class="sxs-lookup"><span data-stu-id="ea8d7-109">Return Value</span></span>  
 <span data-ttu-id="ea8d7-110">如果该方法成功; 则为 S_OK否则为 E_FAIL 或某些其他错误代码。</span><span class="sxs-lookup"><span data-stu-id="ea8d7-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ea8d7-111">要求</span><span class="sxs-lookup"><span data-stu-id="ea8d7-111">Requirements</span></span>  
 <span data-ttu-id="ea8d7-112">**标头：** CorSym.idl、 CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ea8d7-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ea8d7-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ea8d7-113">See Also</span></span>  
 [<span data-ttu-id="ea8d7-114">ISymUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="ea8d7-114">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)