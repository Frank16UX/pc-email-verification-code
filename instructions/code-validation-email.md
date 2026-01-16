# Account Verification Code Email Templates - Design Prompt

## Project Overview
Design 3 distinct account verification code email templates for Pampered Chef. Each template should include a **6-digit numeric verification code only** (no magic links). All designs must follow Pampered Chef's existing Cookbook design system.

---

## Design Analysis & Best Practices

### Reference Examples Analysis

#### Walmart Email Template
- **Approach**: Straightforward, security-focused messaging
- **Key Elements**:
  - Clear, direct subject line: "Your verification code"
  -   - Contextual messaging about code validity (15-minute expiration)
  -     - Security reassurance: "We will never call or text you to request this code"
  -       - Privacy/security information in footer
    - Instructions for account recovery if code wasn't requested
      - Clean, corporate layout with prominent code display
        - Footer with social links and company details
        
        #### Claude.ai Example
        - **Approach**: Minimalist, code-centric design
        - **Key Elements**:
          - Minimal copy, maximum focus on the code itself
            - 6-digit code displayed in large text on contrasting background
              - Simple instruction: "Copy and paste the temporary verification code"
                - One optional action: ignore if not requested
                  - Branded with logo but stays out of the way
                    - Clean typography hierarchy
                    
                    #### Buffer Example
                    - **Approach**: CTA-button focused with trust-building messaging
                    - **Key Elements**:
                      - Prominent centered button for confirmation action
                        - Clear *why* messaging: explains purpose of verification
                          - Security and feature-unlocking benefits highlighted
                            - Support resources linked ("we're here to help")
                              - Professional but friendly tone
                                - Copy that guides user toward action
                                  - Footer with support options
                                  
                                  #### Layers/Inside.com Examples
                                  - **Approach**: Frictionless and community-focused
                                  - **Key Elements**:
                                    - Direct, concise messaging
                                      - Code prominently featured
                                        - Reassurance for security: "safely ignore" if not requested
                                          - Trust-building through transparency
                                            - Optional: notification preference management
                                              - Emoji/personality elements (when brand-appropriate)
                                              
                                              ### Synthesized Best Practices
                                              
                                              1. **Code Prominence**: The 6-digit code should be the visual focal point—use size, color, spacing, and contrast strategically
                                              2. **Clear Purpose**: Explain why the verification is happening and what happens next
                                              3. **Urgency + Reassurance**: Mention code expiration (typically 10-15 minutes) and include a "wasn't you?" recovery path
                                              4. **Copy Tone**: Range from minimal/direct to friendly/helpful depending on brand voice
                                              5. **Trust Elements**:
                                                 - Security messaging about never requesting code via phone/text
                                                    - Privacy policy/security information in footer
                                                       - Optional: notification preference links
                                                       6. **Visual Hierarchy**: 
                                                          - Subject line (clear and scannable)
                                                             - Greeting or context (optional)
                                                                - Code (largest/most prominent)
                                                                   - Secondary CTA or support info
                                                                      - Footer with company details
                                                                      7. **Mobile-First**: Ensure code is readable on all screen sizes
                                                                      8. **Accessibility**: High contrast, readable fonts, proper semantic structure
                                                                      
                                                                      ---
                                                                      
                                                                      ## Design Specifications
                                                                      
                                                                      ### Template Requirements
                                                                      
                                                                      You will create **3 distinct designs**, each with a different strategic approach:
                                                                      
                                                                      **Template 1: Direct & Efficient**
                                                                      - Minimal copy, maximum code visibility
                                                                      - Fast scanning, clear action path
                                                                      - Ideal for users who want to verify quickly with no distractions
                                                                      - Focus: Code + immediate context (expiration, recovery)
                                                                      
                                                                      **Template 2: Trust-Focused & Branded**
                                                                      - Emphasize Pampered Chef brand personality
                                                                      - Balance code with reassuring messaging
                                                                      - Include security confidence-building elements
                                                                      - Focus: Why verification matters + warm brand expression
                                                                      
                                                                      **Template 3: Interactive & Helpful**
                                                                      - CTA-oriented with optional secondary actions
                                                                      - More generous copy explaining benefits
                                                                      - Support resources visible
                                                                      - Focus: Guide user through process with brand as helpful guide
                                                                      
                                                                      ### Technical Requirements
                                                                      
                                                                      - **Code Format**: Exactly 6-digit numeric code (use placeholder: `{VERIFICATION_CODE}`)
                                                                      - **Design System**: Follow all Pampered Chef Cookbook design system guidelines (colors, typography, spacing, components)
                                                                      - **Responsive**: Ensure mobile compatibility (test at 480px, 768px, 1024px+)
                                                                      - **Accessibility**: 
                                                                        - WCAG AA contrast compliance
                                                                          - Semantic HTML structure
                                                                            - Readable font sizes (minimum 14px for body text)
                                                                              - Proper heading hierarchy
                                                                                - Alt text for images/logos
                                                                                - **Email Client Support**: Test across major email clients (Gmail, Outlook, Apple Mail, etc.)
                                                                                - **Code Structure**: 
                                                                                  - Inline CSS (for email client compatibility)
                                                                                    - Minimal external dependencies
                                                                                      - Fallback fonts and colors
                                                                                        - Proper table-based layout or modern email framework
                                                                                        
                                                                                        ### Content Placeholders
                                                                                        
                                                                                        Use these variables for dynamic content:
                                                                                        - `{USER_NAME}` - Recipient's first name
                                                                                        - `{VERIFICATION_CODE}` - 6-digit code
                                                                                        - `{EXPIRATION_TIME}` - Code expiration duration (e.g., "15 minutes")
                                                                                        - `{COMPANY_NAME}` - "Pampered Chef"
                                                                                        - `{SUPPORT_EMAIL}` - Support contact email
                                                                                        - `{SECURITY_POLICY_URL}` - Link to security/privacy info
                                                                                        
                                                                                        ### Subject Line Options
                                                                                        
                                                                                        Provide 2-3 subject line variations for each template that are:
                                                                                        - Clear and scannable
                                                                                        - Action-oriented
                                                                                        - Trustworthy tone
                                                                                        - Under 50 characters when possible
                                                                                        
                                                                                        ---
                                                                                        
                                                                                        ## Deliverables
                                                                                        
                                                                                        For each of the 3 templates, provide:
                                                                                        
                                                                                        1. **HTML Code** - Production-ready email HTML with inline CSS
                                                                                        2. **Visual Preview** - Screenshot/description of how it appears
                                                                                        3. **Strategy Document** including:
                                                                                           - Design rationale (why this approach works)
                                                                                              - Key USPs vs. other templates
                                                                                                 - Ideal use case/audience segment
                                                                                                    - Copy variations (3 subject lines, body variations)
                                                                                                    4. **Testing Checklist**:
                                                                                                       - Mobile responsiveness verification
                                                                                                          - Email client rendering checks
                                                                                                             - Code display clarity at different sizes
                                                                                                                - Contrast and accessibility confirmation
                                                                                                                5. **Implementation Notes**:
                                                                                                                   - Variable insertion points
                                                                                                                      - Personalization opportunities
                                                                                                                         - Tracking/analytics integration points
                                                                                                                            - CRM system compatibility notes
                                                                                                                            
                                                                                                                            ---
                                                                                                                            
                                                                                                                            ## Design Guidance
                                                                                                                            
                                                                                                                            - **Brand Consistency**: Maintain Pampered Chef's visual identity throughout
                                                                                                                            - **White Space**: Use generous spacing around the verification code for emphasis
                                                                                                                            - **Color**: 
                                                                                                                              - Consider brand primary colors for code highlighting
                                                                                                                                - Use neutral backgrounds for code readability
                                                                                                                                  - Ensure sufficient contrast
                                                                                                                                  - **Typography**: 
                                                                                                                                    - Verification code: Large, monospace or distinctive font
                                                                                                                                      - Headings: Clear visual hierarchy
                                                                                                                                        - Body: Highly readable without being oversized
                                                                                                                                        - **Imagery**: 
                                                                                                                                          - Optional: brand logo/mascot (use sparingly)
                                                                                                                                            - Consider: security badge or verification icon
                                                                                                                                            - **Footer**: 
                                                                                                                                              - Company legal information
                                                                                                                                                - Links to privacy/security policies
                                                                                                                                                  - Unsubscribe/preference center link
                                                                                                                                                    - Social media (if applicable)
                                                                                                                                                    
                                                                                                                                                    ---
                                                                                                                                                    
                                                                                                                                                    ## Success Criteria
                                                                                                                                                    
                                                                                                                                                    Each template should:
                                                                                                                                                    - [ ] Display the 6-digit code as the primary visual focus
                                                                                                                                                    - [ ] Be readable on mobile devices without horizontal scrolling
                                                                                                                                                    - [ ] Render correctly in Gmail, Outlook, Apple Mail, and Yahoo Mail
                                                                                                                                                    - [ ] Maintain accessibility standards (WCAG AA)
                                                                                                                                                    - [ ] Reflect Pampered Chef brand guidelines
                                                                                                                                                    - [ ] Include security/reassurance messaging
                                                                                                                                                    - [ ] Provide clear next steps or recovery options
                                                                                                                                                    - [ ] Differentiate meaningfully from the other 2 templates
                                                                                                                                                    - [ ] Include copy that guides users toward verification action
                                                                                                                                                    - [ ] Load and display without images (graceful degradation)
                                                                                                                                                    
                                                                                                                                                    ---
                                                                                                                                                    
                                                                                                                                                    ## Notes for Implementation
                                                                                                                                                    
                                                                                                                                                    - These are transactional emails; they don't require unsubscribe per regulations, but including preference management builds trust
                                                                                                                                                    - Test with real code examples (e.g., "123456") to ensure proper display
                                                                                                                                                    - Consider A/B testing these 3 approaches to see which drives highest verification rates
                                                                                                                                                    - Monitor email client rendering and adjust as needed
                                                                                                                                                    - Ensure code is delivered securely and that old/expired codes are invalidated properly on the backend