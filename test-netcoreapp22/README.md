# Smartsheet SDK .NET Core 2.2 Test Application

This is a test console application to verify that the Smartsheet C# SDK works correctly with .NET Core 2.2 after multi-targeting to netstandard2.0.

## Prerequisites

- .NET Core 2.2 SDK/Runtime installed
- A Smartsheet access token

## How to Build

```bash
cd test-netcoreapp22
dotnet build
```

## How to Run

```bash
dotnet run <your_smartsheet_access_token>
```

Replace `<your_smartsheet_access_token>` with your actual Smartsheet API access token.

## What This Test Does

1. Initializes the Smartsheet client with the provided access token
2. Attempts to list the user's sheets
3. Displays the first 5 sheets (if any exist)
4. Confirms that the SDK is working correctly with .NET Core 2.2

## Expected Output

If successful, you should see:
```
Testing Smartsheet C# SDK with .NET Core 2.2
==============================================

1. Initializing Smartsheet client...
   ✓ Client initialized successfully

2. Fetching user's sheets...
   ✓ Successfully retrieved X sheet(s)

   First 5 sheets:
   - Sheet Name 1 (ID: 123456789)
   - Sheet Name 2 (ID: 987654321)
   ...

✓ Test completed successfully!

The SDK is working correctly with .NET Core 2.2
```

## Notes

- .NET Core 2.2 is out of support, but this test verifies backward compatibility
- The SDK uses the netstandard2.0 target when running on .NET Core 2.2
- You may see warnings about .NET Core 2.2 being out of support - this is expected

## Troubleshooting

If you encounter errors:
- Verify your access token is valid
- Check that you have internet connectivity
- Ensure .NET Core 2.2 SDK/Runtime is properly installed
- Review the error message and stack trace for details
